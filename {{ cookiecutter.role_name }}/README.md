# {{ cookiecutter.role_name }} 

{{ cookiecutter.project_short_description }}

## File structure

* `main.yml`
* `setup-Debian` / `setup-RedHat`: Add ppa/repositories, update cache, install packages, ...
* `configure-Debian` / `configure-RedHat`: Apply templates, copy files, restart services, ...
* vars:
    * `Debian.yml`: Debian related variables (like packages which name changes from one distribution to the other).
    * `RedHat.yml`: Same for RedHat.
    * `host_vars.yml`: Declare variables for testing with Vagrant.

## Vagrant

Edit machine configuration in `machine_definition.yml`.

Vagrant will provision a box with the configuration just typing:

    $ cd vagrant
    $ vagrant status

      Current machine states:

      trusty64                  not created (virtualbox)
      centos7                   not created (virtualbox)

      This environment represents multiple VMs. The VMs are all listed
      above with their current state. For more information about a specific
      VM, run `vagrant status NAME`.


    $ vagrant up trusty64

## Kitchen-Ansible

Install kitchen-ansible gem

    $ sudo gem install test-kitchen kitchen-ansible

Check [github repo](https://github.com/neillturner/kitchen-ansible) for examples.

## Author

Created in {{ cookiecutter.year }} by {{ cookiecutter.full_name }}

## License

{{ cookiecutter.license }}
