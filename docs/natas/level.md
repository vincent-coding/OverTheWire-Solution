# Natas - Level 0

?> **Level Info:** Username: natas0<br>
Password: natas0<br>
URL:      http://natas0.natas.labs.overthewire.org

These levels are dedicated to the web page.<br>
When you click on the link on the first page available [here](http://natas0.natas.labs.overthewire.org), they will ask you to log in.
- **Username**: natas0
- **Password**: natas0

Once you are logged in, simply right-click and `view the source code` for the page.<br>
You'll have to get a result like this:
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
<script>var wechallinfo = { "level": "natas0", "pass": "natas0" };</script></head>
<body>
<h1>natas0</h1>
<div id="content">
You can find the password for the next level on this page.

<!--The password for natas1 is gtVrDuiDfck831PqWsLEZy5gyDz1clto -->
</div>
</body>
</html>
```
As you can see, the password is hidden using the `<!--` and `-->`.<br>
So the password is: `gtVrDuiDfck831PqWsLEZy5gyDz1clto`

So you can move on to the next level.