PRM
========

Ansible role that creates and synchronizes a .deb or .rpm repository using **PRM** (https://github.com/dnbert/prm).

It installs all the necessary tools, copies local packages to the remote host and then creates/updates a repository. All the defaults are Debian-oriented.

Check the documentation for PRM at https://github.com/dnbert/prm .

Requirements
------------

Assumes that the host is ansible-ready (check **ansible-bootstrap** repository).

Role Variables
--------------

* `prm_pkg_state`: Specifies if this role will garantee that the packages are installed or installed and updated. Possible values: `installed` and `latest`. Defaults to `installed`.
* `prm_gem_state`: Specifies if this role will garantee that the gems are installed or installed and updated. Possible values: `installed` and `latest`. Defaults to `installed`.
* `prm_gem_user_install`: Install PRM gem system-wide or to running user only. Defaults to "no".
* `prm_repo_type`: Create/update "deb" or "rpm" repository. Defaults to "deb".
* `prm_repo_release`: Codename of the distribution release to be used. Defaults to "wheezy".
* `prm_repo_path`: Path where to create/update the repository. Defaults to `/srv/repo`.
* `prm_repo_directory`: Path where to move the uploaded packages from. Defaults to `/srv/repo`.
* `prm_repo_gpg`: GPG key used to sign repository metadata. Defaults to "repo".
* `prm_repo_arch`: Arch for the repository. Defaults to "amd64".
* `prm_repo_deb_component`: Defaults to "main". Only applies to "deb" repositories.
* `prm_repo_deb_nocache`: Don't use md5sum cache. Defaults to "no".

License
-------

MIT

Author Information
------------------

Thanks to @dnbert for creating PRM!

[GitHub project page](https://github.com/mtpereira/ansible-passenger)

[Manuel Tiago Pereira](http://mtpereira.github.io)
