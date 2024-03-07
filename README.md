<pre>
sudo su; 
apt -y install gcc make php-pear php-pdo php-dev build-essential unixodbc-dev;
pecl channel-update pecl.php.net; 
pecl install sqlsrv pdo_sqlsrv; 
echo 'extension=pdo_sqlsrv.so' > /etc/php/8.2/mods-available/pdo_sqlsrv.ini; 
echo 'extension=sqlsrv.so' > /etc/php/8.2/mods-available/sqlsrv.ini; 
phpenmod pdo_sqlsrv sqlsrv;
</pre>
