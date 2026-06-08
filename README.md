api/ip.php
<?php
$ip = $_SERVER['REMOTE_ADDR'];
$ua = $_SERVER['HTTP_USER_AGENT'];
$time = date('Y-m-d H:i:s');
$log = $time . " | IP: " . $ip . " | 设备信息: " . $ua . "\n";
file_put_contents("log.txt", $log, FILE_APPEND);
header('Location: https://www.baidu.com');
exit;
?>
