# line-us
basic line-us library/example using php

sends an array of commands to the line-us drawing machine via a Socket connection.

more or less a port of https://github.com/Line-us/Line-us-Programming/blob/master/Python/HelloWorld.py#L1

The line-us github is located at: https://github.com/Line-us/Line-us-Programming


## howto

- clone the repository
- download the lineUs.php file to your project
- add the lineUs class to your project by including it ``` include("../path/to/file/lineUs.php");```
- use the php line us class by doing ``` $lineUs->send($gcode);```
- be sure that the php server is running on the same wifi network as the Line-Us Robot

## extra

#### send()
```php
echo $lineUs -> send($gcode,[$addr],[$port]);
```
Gcode sent as 'String'  
Default Address: line-us.local  
Default port: 1337  
Returns line-us bot output  

#### sendArray()
```php
echo $lineUs -> sendArray($gcode,[$addr],[$port]);
```
Gcode sent as 'Array'  
Default Address: line-us.local  
Default port: 1337   
Returns line-us bot output  

#### findIp()
```php
echo $lineUs -> findIp([$port]);
```
return the first ip found with the port
Default port: 1337  
