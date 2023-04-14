# Section 1
The PHP Crude CRUD Application is designed for understanding and working with dynamic data-driven web applications.  
It creates a LAMP server on the local machine, utilizing MariaDB as the MySQL database to store and retrieve employee information. The application allows users to search for employees based on specified credentials, 
add new employees to the database, and view employee data in the form of an HTML table.
# Section 2
The general steps to create an entirely new application architecture and stack from the ground up for deploying the PHP Crude CRUD app involve several key steps. First, provision a virtual machine using Oracle's VirtualBox on your local machine. Next, install Apache and PHP on the virtual machine to create a local server for hosting PHP and HTML files. Store the files in the /var/www/html directory on the virtual machine. Finally, deploy the PHP Crude CRUD Application using the IP address and file location on the server in a web browser to access and interact with the application.
# Section 3
Disk: 20GB
CPU: 1
RAM: 2048 MB
# Section 4
To create a VirtualBox Virtual Machine, first, download and install VirtualBox from the official website. Once installed, launch VirtualBox and click on "New" to open the "New Virtual Machine Wizard". Give the virtual machine a name that will help you recognize it easily. Next, choose the type of operating system you want to install on the virtual machine, such as Linux or Ubuntu 64-bit. Allocate memory (RAM) for the virtual machine to use during its operation.

Create a virtual hard drive for the virtual machine to store its data, and choose the file type for the virtual hard drive, such as VDI. Choose the storage option for the virtual hard drive, such as dynamically allocated, and set the size of the virtual hard drive, for example, 20 GB. Click "Create" to create the virtual machine with the specified settings.

Configure the virtual machine settings, such as the number of CPUs, display settings, and network settings, according to your requirements. Start the virtual machine to boot up the operating system installation process. Follow the on-screen instructions to install the operating system on the virtual machine. You may also choose to install VirtualBox Guest Additions, which are optional additional features and performance improvements for the virtual machine.

Once the installation is complete restart it, the virtual machine is now ready to use. You can interact with it as if it were a physical machine on your computer, and install any additional software or applications as needed.
# Section 5
Download and install VirtualBox from the Oracle VM VirtualBox website.
Create a new virtual machine with Ubuntu 20.04 as the operating system.
SSH into the virtual machine using the terminal.
Run the commands sudo apt update and sudo apt upgrade to update and upgrade the system.
Follow any prompts during the update and upgrade process.
Install additional software or applications as needed.
# Section 6
1. Update and upgrade the server using the commands: $ sudo apt update and $ sudo apt upgrade.
2. Install Apache 2 by running the command: $ sudo apt install apache2.
3. Install PHP by running the command: $ sudo apt install libapache2-mod-php.
4. Restart the Apache service to load PHP with the command: $ sudo systemctl restart apache2.
# Section 7
1. Update and upgrade system packages using the following command: $ sudo apt update && sudo apt upgrade.
2. Install MySQL server with the command: $ sudo apt install mysql-server.
3. Check the status of MySQL with the command: $ sudo systemctl status mysql.
4. Restart MySQL server with the command: $ sudo systemctl restart mysql.
5. Log in to MySQL server as the root user with the command: $ sudo mysql -u root -p.
# Section 8
The connection and credential configuration information is stored in a file called credentials.php.
The credentials.php file is located within the phpcrudecrudapp directory.
The absolute path of the credentials.php file is /var/www/html.
You can check and modify the connection and credential information in the credentials.php file as needed to configure PHP to connect to the database.
# Section 9
Download the key INET4031_Spring_2023.pem and move it to your .ssh directory on your local machine.
Create a zip file of your PHP application on your server: tar -zcvf ayubfarah_phpcrudecrud.tar.gz phpcrudecrudapp/
Use scp with the provided SSH key to send the zipped PHP directory to the server: scp -i .ssh/INET4031_Spring_2023.pem ayubfarah_phpcrudecrud.tar.gz ubuntu@18.119.121.213:.
SSH into the server: ssh -i .ssh/INET4031_Spring_2023.pem ubuntu@18.119.121.213
Extract the zip file and move the contents to a directory named _phpcrudecrud: tar -xvf ayubfarah_phpcrudecrud.tar.gz
Move the phpcrudecrudapp directory to /var/www/html directory: sudo cp -R ayubfarah_phpcrudecrudapp/ /var/www/html
Check that your application is located in /var/www/html directory.
Access your PHP Crude CRUD Application in the browser by typing the server's IP address followed by /_phpcrudecrudapp, e.g., http://18.119.121.213/_phpcrudecrudapp.
# Section 10
Test Apache: Launch a web browser and enter the IP address or address of the VM. The default Apache web page should be displayed.

Test PHP: Create a PHP file with phpinfo() function in the Apache document root directory (/var/www/html) to ensure PHP is installed and operating properly. Save the file, launch the web browser, and enter the server's IP address followed by the filename (e.g., http://server_ip/test.php). You should see a webpage displaying PHP information, confirming PHP is working correctly.






