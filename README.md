# Setup_visualhost

/* Set the visualhost on xampp
      file1_path = "c/windows/system32/drivers/etc/hosts"   // for set the host of project(that is main file), without permission of notepad this file not access, aftr  write ans save another project is not run 
        127.0.0.1 credit1234.com
     * 
     * file2_path = "c/xampp/apache/conf/extra/httpd-vhosts.conf"    // write the visualhost rule for each project
     <VirtualHost *:80>
            ServerName www.projectname.com
            DocumentRoot "C:\xampp\htdocs\projectname"
            SetEnv APPLICATION_ENV "development"
            <Directory "C:\xampp\htdocs\projectname">
                DirectoryIndex index.php
                AllowOverride All
                Order allow,deny
                Allow from all
                Require all granted
            </Directory>
        </VirtualHost>
    */
