# Koha installation processes

▪ Koha community 

▪ Download koha

▪ Installation current version 

▪ Open terminal

▪ Enter to root node by using system password

▪ ``$ sudo su`` - this command used for enter to root 
node

``sudo apt-get update`` - (To update the system)

``sudo apt-get upgrade`` - (to upgrade the system) 

▪ Let choose stable version command to create Repository

▪ ``echo ‘deb http://debian.koha-community.org/koha stable 
main’ | sudo tee /etc/apt/sources.list.d/koha.list``

▪ Set up package source by adding GPG key to your system 
``wget -q -0- https://debian.koha-community.org/koha/gpg.asc | sudo apt-key add –``

▪ Update the system before installing Koha 
 ``sudo apt-get update``

▪ Instal Koha:
 ``sudo apt-get install koha-common``

If correct yes/no [y/n] 

Choose y and press enter then start to install koha 

▪ Edit network setting: used to fix code number
 (Interaport and OPACport) 

 ``sudo gedit /etc/koha/koha-sites.conf``

▪ Install the database: Either you can install MariaDB or MySQL

▪ Here we use the mySQL command to install database
 ``sudo apt-get install mysql-server``

If correct yes/no [y/n]
Choose y and press enter then start to install database 

▪ Set up Apache

 ``sudo a2enmod rewrite``

 ``sudo a2enmod cgi``

 ``sudo service apache2 restart``

Execute these of three Command by order to confirm apache

▪ Create a koha instance: it is used for only mysql locally

 ``sudo koha-create – create -db libraryname``

▪ Edit port in Apache: Apache port to config file 

 ``sudo gedit /etc/apache2/ports.conf``

▪ Here fix the port number to Apache

▪ Disable Apache default site

 ``sudo a2dissite 000- default`` 

 ``sudo a2enmod deflate``

 ``sudo a2ensite library``

 ``sudo service apache2 restart``

▪ To get master Password:

 ``sudo koha-passwd library``

- Master Password is used to login to the KOHA administration and work on the Webinstaller and Onboarding tools. 
