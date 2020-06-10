# Natas - Level 3

?> **Level Info:**<br>*Username:* natas4<br>*URL:* http://natas4.natas.labs.overthewire.org

!> This level is more advanced because it introduces to the `Burp` software. Download [here](https://portswigger.net/burp).

This tutorial requires Burp and redirect requests. You can follow this tutorial [here](https://portswigger.net/burp/documentation/desktop/penetration-testing/configuring-your-browser).

Once all these prerequisites are met.<br>
We can move on to the tutorial!

Like every other level you've ever done, you have to log in:
- **Username:** natas4
- **Password:** Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ

When you get to the page you should have something that looks like this:<br>
<img src="./assets/natas/lvl3.png" /><br>
It's so much to run `Burp Suite`.<br>
Check that you have reconfigured your proxy.<br>
<img src="./assets/natas/burp-start.png" /><br>
When it is launched they will ask you to choose what type of project you want.<br>
Choose the option `Temporary project`.<br>
<img src="./assets/natas/burp-project.png" /><br>
If you are asked for a configuration, choose the option as shown in the picture below.<br>
<img src="./assets/natas/burp-config.png" /><br>
Once the software is launched you will arrive on a home page.
<img src="./assets/natas/burp-ui.png" />
Go now to the Proxy, and activate the proxy of your browser.<br>
Once you have done this press `Refresh Page`.<br>
**If all was well done the page should load in a vacuum.**<br>
If not, check the proxy, make sure the `Intercept is:` button is `on` and not `off` and try again.

In the proxy tab, then intercept, then raw you should have a result like this:
```
GET /index.php HTTP/1.1
Host: natas4.natas.labs.overthewire.org
Authorization: Basic bmF0YXM0Olo5dGtSa1dtcHQ5UXI3WHJSNWpXUmtnT1U5MDFzd0Va
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.138 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Referer: http://natas4.natas.labs.overthewire.org/index.php
Accept-Encoding: gzip, deflate
Accept-Language: fr-FR,fr;q=0.9,de-DE;q=0.8,de;q=0.7,en-US;q=0.6,en;q=0.5
Cookie: __utma=176859643.1932855269.1591734175.1591734175.1591734175.1; __utmz=176859643.1591734175.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none)
Connection: close
```
Do you see the line where `Referer` is marked?<br>
Well, she's the one for us.<br>
We will therefore replace the line containing
```
Referer: http://natas4.natas.labs.overthewire.org/index.php
```
by
```
Referer: http://natas5.natas.labs.overthewire.org/
```
Once this is done, click on the foward button, the request would be sent to the server.<br>
If we go back to the web page, we see that the content to be changed.<br>
<img src="./assets/natas/lvl3-1.png" />
We now have your password for the next level!<br>
Don't forget to disable the proxy! :wink: