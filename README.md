# dspace-box

Installation of DSpace7 via ansible.

Documentation see also
* https://wiki.lyrasis.org/display/DSDOC7x/Release+Notes
* https://wiki.lyrasis.org/display/DSDOC7x/Installing+DSpace
* https://wiki.lyrasis.org/display/DSPACE/Try+out+DSpace+7
* https://wiki.lyrasis.org/display/DSPACE/Running+DSpace+7+with+Docker

**NOTE**:
* This project should make it possible to deploy DSpace 7 in a virtual box or VM (if ansible playbook is used directly). It does not use the DSpace docker image.

## Installation on local system for testing

Prerequisites
* [Git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Perform the following steps in the terminal (Linux / macOS) or in the GitBash (Windows).
```

git clone https://github.com/TIBHannover/dspace-box.git
cd dspace-box

```

When the installation is complete (a few minutes, depending on the download speed), dspace can be opened in the browser

For Dev:

<http://192.168.98.111:4000/>

Initial login via test@test.edu / admin

For changes - the env vars at `ansible/vars/main.yml` can be modified. Example - 
```
  ip_client: 192.168.98.111
  ip_server: 192.168.98.111
  server_port: 8080
  client_port: 4000
  ssl_enabled_client: false
  ssl_enabled_server: false
  ui_namespace: /
  server_namespace: /server 
  admin_email: test@test.edu
  admin_first_name: admin
  admin_last_name: user
  admin_password: admin
  work_user: vagrant

```
And, 

```
env: "prod" | "dev" 
```

can be configured in the same
