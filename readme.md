## Simple Magento Vagrant

A very simple Magento enviorment provisioner for Vagrant.

## Getting Started

### Prerequisites

- Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Install [Vagrant](https://www.vagrantup.com/)
- Clone or download this repository of your project:https://github.com/LEGreen1984/magento-environment.git

- Go to the [magento](https://magento.com/tech-resources/download) download site and download the open source version as a TAR file

<img src='magento.png'>

- Next, create a directory called ‘magento’ with the path ‘~/magento’.

<img src='path.png'>

- Copy and paste the tar file into this folder. This is vital because the ‘synced folder’ route is hardcoded.

- In your project directory, run vagrant up


## Usage

In your browser, head to 192.168.10.100/magento

Creating Magento Database

By now, all the packages required to support Magento 2 installation are ready. Next, we’ll create a blank database for Magento. To accomplish this, first, login to the MYSQL server:

1.	$ sudo mysql -u root -p

You will be prompted for your MYSQL Server password. Enter the password and click Enter to continue.

Run the following commands to create a new database titled Magento:

2.	CREATE DATABASE  magento;

Next, create a user called magentouser and assign the user a new password, using the commands below:

3.	CREATE USER'magentouser'@'localhost'IDENTIFIED BY'EnterNewPasswordHere';

Then grant, the user you’ve created unlimited access to the new database:

4.	GRANT ALL ON magento.* TO'magentouser'@'localhost'IDENTIFIED BY'EnterPasswordHere'WITH GRANT OPTION;

Save the changes and exit:

5.	FLUSH PRIVILEGES;


6.	EXIT;
