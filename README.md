# Duraspace DSpace 7 Box

Installation of DSpace7 via ansible.

Documentation see also
* https://wiki.lyrasis.org/display/DSDOC7x/Release+Notes
* https://wiki.lyrasis.org/display/DSDOC7x/Installing+DSpace
* https://wiki.lyrasis.org/display/DSPACE/Try+out+DSpace+7
* https://wiki.lyrasis.org/display/DSPACE/Running+DSpace+7+with+Docker

**NOTE**:
* DSpace 7 is still a Beta version and under active development. It is not recommended to install it in production!
* This project should make it possible to try out DSpace 7 in a virtual box. It uses the DSpace docker image.

## Installation on local system for testing

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

<http://192.168.98.111:4000/>

Initial login via test@test.edu / admin
