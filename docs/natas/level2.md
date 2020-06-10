# Natas - Level 2

?> **Level Info:**<br>*Username:* natas3<br>*URL:* http://natas3.natas.labs.overthewire.org

As for the other levels you have to log in:
- **Username:** natas3
- **Password:** sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14

As usual, display the source code of the page.<br>
It should look like this:
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
<script>var wechallinfo = { "level": "natas3", "pass": "sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14" };</script></head>
<body>
<h1>natas3</h1>
<div id="content">
There is nothing on this page
<!-- No more information leaks!! Not even Google will find it this time... -->
</div>
</body></html>
```
If you view the source code, you will see a comment in the `<!--` and `-->` tags.<br>
This message means that even Google can't find it. Let's check it out :wink:

Each website, can create a file named `robots.txt` to prevent certain pages from being browsed by search engine bots.<br>
So we're going to check this page.<br>
The url of the current web page should look like this
```
view-source:http://natas3.natas.labs.overthewire.org/
```
or
```
http://natas3.natas.labs.overthewire.org/
```

If you are in the first case, delete the source view.<br>
Now that everyone has the same url, we will add the robots.txt to the url, which gives:
```
http://natas3.natas.labs.overthewire.org/robots.txt
```
One page should load.<br>
This page should contain something like this:<br>
```
User-agent: *
Disallow: /s3cr3t/
```
The `User-Agent` means that all robots must follow the following instruction.<br>
The next line means that bots are not allowed to access the next folder: `/s3cr3t/`

So we will remove the `robots.txt` from the url and replace it with the name of the folder.
```
http://natas3.natas.labs.overthewire.org/s3cr3t/
```
You should see a page like this:<br>
<img src="./assets/natas/lvl2.png" /><br>
Click on the file `users.txt`, the password should be stored in it.<br>
Once opened, the document should look like this:
```
natas4:Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
```
So the password is as follows: `Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ`<br>
So we can move on to the next level.