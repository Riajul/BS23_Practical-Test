# Vagrant Installation
At first install VirtualBox and Vagrant.

Please run below commad to check vagrant is working or not
> vagrant --version

Now, to create vagrant file for master and 2 workers.
Please go to Master and run below command:
> vagrant up

It may takes time when Master is setup then other workers will take less time.
After installing CentOS, please run below command:
> vagrant ssh

It will take login with 'vagrant' user.
To set the root password run
> sudo passwd root

Finally please login with root and you are using VM with Root
> su root