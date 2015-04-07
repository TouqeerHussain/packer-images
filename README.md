#Software Requirements to build and test images OS X / Ubuntu 14.04

	* download Packer version: 0.7.5   -   unzip packer_0.7.5_darwin_amd64.zip -d /usr/sbin
	* download Vagrant version:1.7.2
	* donwload and install VirtualBox version:4.3.26
	* download and install QEMU/KVM   

# Vagrant Packer

### Box for vagrant and OpenStack

Ubuntu: CIS recommended partition layout

	* Ubuntu 14.04 (server)
	* Ubuntu 12.04.04 (server)

CentOS: CIS recommended partition layout

	* CentOS 6.5 (minimal)
	* CentOS 7 (minimal)

Fedora: CIS recommended partition layout

	* Fedora 20 (minimal)
	* Fedora 21 (minimal)

### Usage / Build Images

<pre>
$ packer build CentOS-6.6.json
$ packer build Ubuntu-12.04.4.json 
</pre>
