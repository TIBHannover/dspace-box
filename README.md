# dspace-box

Installation of DSpace7 via ansible.

Documentation see also
* https://wiki.lyrasis.org/display/DSDOC7x/Release+Notes
* https://wiki.lyrasis.org/display/DSDOC7x/Installing+DSpace
* https://wiki.lyrasis.org/display/DSPACE/Try+out+DSpace+7
* https://wiki.lyrasis.org/display/DSPACE/Running+DSpace+7+with+Docker

**NOTE**:
* This project should make it possible to deploy DSpace 7 in a virtual box or VM (if ansible playbook is used directly). It uses the DSpace docker images.
* The default docker-images used here are not intended for productive use. You can deploy your own productive docker images through this project (via Ansible) by setting your images in the `dspace_**_image` variables.

## Installation on local system for local testing

Prerequisites
* [Git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Perform the following steps in the terminal (Linux / macOS) or in the GitBash (Windows).

```
git clone https://github.com/TIBHannover/dspace-box.git
cd dspace-box
vagrant up
```

When the installation is complete (a few minutes, depending on the download speed), dspace can be opened in the browser

For local Vagrant VirtualBox:

<http://192.168.56.111:4000/>

Initial login via test@test.edu / admin

For changes - the vars at `ansible/group_vars/main.yml` can be modified. Example -  

```
dspace_frontend_replicas: 4
```
