# testing
mysql database or table backup in php


<?php
include "table_backup.php";
$backup_file = 'db-backup-'.time().'.sql';

// get backup
$mybackup = backup_tables("localhost","root","","test","*");

// save to file
$handle = fopen($backup_file,'w+');
fwrite($handle,$mybackup);
fclose($handle);

?>