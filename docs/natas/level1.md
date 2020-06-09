# Natas - Level 1

?> **Level Info**: Username: natas2<br>URL: http://natas2.natas.labs.overthewire.org

This level is not very complicated.<br>
Start a session and enter the following credentials:
- **Username:** natas2
- **Password:** ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi

Once connected, they simply need to access the source code of the page (via a <kbd>&#8963;</kbd>+ <kbd>U</kbd>, for example).

```html
<html>
<head>
<!-- This stuff in the header has nothing to do with the level -->
<link rel="stylesheet" type="text/css" href="http://natas.labs.overthewire.org/css/level.css">
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/jquery-ui.css" />
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/wechall.css" />
<script src="http://natas.labs.overthewire.org/js/jquery-1.9.1.js"></script>
<script src="http://natas.labs.overthewire.org/js/jquery-ui.js"></script>
<script src=http://natas.labs.overthewire.org/js/wechall-data.js></script><script src="http://natas.labs.overthewire.org/js/wechall.js"></script>
<script>var wechallinfo = { "level": "natas2", "pass": "ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi" };</script></head>
<body>
<h1>natas2</h1>
<div id="content">
There is nothing on this page
<img src="files/pixel.png">
</div>
</body></html>
```

As you can see, the password is not directly written in the page, but you can see that an image exists.<br>
All you have to do is click on the link in `src` of the `img` tag.<br>
This should redirect you to a black page without any images. <br>
Look at the url, you should have something like this:
```
http://natas2.natas.labs.overthewire.org/files/pixel.png
```
Delete `pixel.png` and press `Enter`.<br>
You'll be redirected to a page that should look like this.<br>
<img src="./assets/natas/lvl1.png" /><br>
Click on the file `users.txt`.<br>
You'll be redirected to a page that contains your text and you'll see that:
```
# username:password
alice:BYNdCesZqW
bob:jw2ueICLvT
charlie:G5vCxkVV3m
natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
eve:zo4mJWyNj2
mallory:9urtcpzBmH
```
If you look, you have a line containing the level 2 password:
```
natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
```
So the password is: `sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14`<br>
So you can go to the next level.