# wp-config
This is a cheatsheet for WordPress configuration file settings.


##Disable FTP authorization for filesystem changes - change FS_METHOD to 'direct'
`php
define( 'WP_DEBUG', true );
define('FS_METHOD', 'direct');
define('FS_CHMOD_DIR', (0705 & ~ umask()));
define('FS_CHMOD_FILE', (0604 & ~ umask()));
`
