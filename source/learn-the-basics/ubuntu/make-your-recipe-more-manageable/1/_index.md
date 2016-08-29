## 1. Create a cookbook

First, from your <code class="file-path">~/chef-repo</code> directory, create a <code class="file-path">cookbooks</code> directory.

```bash
# ~/chef-repo
$ mkdir cookbooks
```

Now run the `chef` command to generate a cookbook named `learn_chef_apache2`.

```bash
# ~/chef-repo/cookbooks
$ chef generate cookbook learn_chef_apache2
```

The <% fp 'cookbooks/learn_chef_apache2' %> part tells Chef to create a cookbook named `learn_chef_apache2` under the <% fp 'cookbooks' %> directory.

Here's the directory structure that the command created.

```bash
# ~/chef-repo/cookbooks
$ tree
.
└── learn_chef_apache2
    ├── Berksfile
    ├── chefignore
    ├── metadata.rb
    ├── README.md
    ├── recipes
    │   └── default.rb
    ├── spec
    │   ├── spec_helper.rb
    │   └── unit
    │       └── recipes
    │           └── default_spec.rb
    └── test
        └── integration
            ├── default
            │   └── serverspec
            │       └── default_spec.rb
            └── helpers
                └── serverspec
                    └── spec_helper.rb

11 directories, 9 files
```

Note the default recipe, named <code class="file-path">default.rb</code>. This is where we'll move our Apache recipe in a moment.