<pre>
sudo su
apt -y install gcc make php-pear php-pdo php-dev build-essential unixodbc-dev;
pecl channel-update pecl.php.net; 
pecl install sqlsrv pdo_sqlsrv; 
echo 'extension=pdo_sqlsrv.so' > /etc/php/8.2/mods-available/pdo_sqlsrv.ini; 
echo 'extension=sqlsrv.so' > /etc/php/8.2/mods-available/sqlsrv.ini; 
phpenmod pdo_sqlsrv sqlsrv;

curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add -;
curl https://packages.microsoft.com/config/ubuntu/16.04/prod.list > /etc/apt/sources.list.d/mssql-release.list
exit
sudo apt-get update
sudo ACCEPT_EULA=Y apt-get install msodbcsql17
</pre>
