#Set up cli xdebug with on Vagrant and PHPStorm

1. ssh into vagrant server `vagrant ssh`
2. update xdebug ini file `sudo vim /etc/php/**php-version**/cli/conf.d/20-xdebug.ini
`
3. in the xdebug ini add  
    `xdebug.remote_host = local ip`   
    `xdebug.remote_autostart = 1`
    
4. run `php7.1 -dxdebug.remote_enable=1 -dxdebug.remote_mode=req -dxdebug.remote_port=9000 -dxdebug.remote_host=10.0.2.2 -dxdebug.remote_connect_back=0 path/to/file`