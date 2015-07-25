## 2. Create a template

Now we'll move the home page to an external file. First, run this command to generate the HTML file for our home page.

```ps
# ~\chef-repo\cookbooks
$ chef generate template learn_chef_iis index.html
```

The file <code class="file-path">index.html.erb</code> gets created under <code class="file-path">learn\_chef\_iis\templates\default</code>.

```ps
# ~\chef-repo\cookbooks
$ tree /F
Folder PATH listing
Volume serial number is 5E71-6BA3
C:.
└───learn_chef_iis
    │   .kitchen.yml
    │   Berksfile
    │   chefignore
    │   metadata.rb
    │   README.md
    │
    ├───recipes
    │       default.rb
    │
    └───templates
        └───default
                index.html.erb
```

The .erb extension simply means that the file can have placeholders. More on that later.

Now copy the contents of the HTML file from your recipe to the new HTML file, <code class="file-path">index.html.erb</code>.

```html-Win32
<!-- ~\chef-repo\cookbooks\learn_chef_iis\templates\default\index.html.erb -->
<html>
  <body>
    <h1>hello world</h1>
  </body>
</html>
```

[COMMENT] If you're using the Atom text editor, running the `atom .` command from your <code class="file-path">cookbooks</code> directory enables you to easily navigate among your cookbook's files.