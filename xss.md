# xss

>XSS全称为Cross Site Scripting，为了和CSS分开简写为XSS，中文名为跨站脚本。<br>该漏洞发生在用户端，是指在渲染过程中发生了不在预期过程中的JavaScript代码执行。XSS通常被用于获取Cookie、以受攻击者的身份进行操作等行为。

分类：
- Non-persistent
- Persistent
  - further divide these two groups into traditional (caused by server-side code flaws) and DOM-based (in client-side code).

>more details below
<br>

## Non-persistent(Reflected XSS)

>简述一下（根据维基百科的话），反射xss是世界上最基本的网络漏洞，这些漏洞都是在客户端提交数据(最常见的是 HTTP 查询参数(例如 HTML 表单提交)给服务器且被服务器端脚本未对内容进行“消毒”，立即用于解析和显示用户页面的结果时显示出来。

<br>

## Persistent(Stored XSS)

>比起Reflected XSS更具破环性。当服务器保存攻击者提供的数据，然后在常规浏览过程中将其永久显示在返回给其他用户的“正常”页面上，并且不进行适当的 HTML 转义时，就会发生该攻击。<br>
>这方面的一个典型例子是在线留言板，用户可以发布 HTML 格式的消息，如果服务器没有进行转义保护就会导致攻击成功。

<br>
使用Persistent XSS的恶意脚本可以自动渲染，不需要单独针对一个受害者或者骗人到第三方网站。

<br>

## DOM-based vulnerabilities

>（大概意思）因为用户需求随时代进步增大，web各种应用程序（大多由JavaScript编写）开始增多，由于JavaScript代码在处理用户输入数据同时将其显示在网页内容中，从而诞生该攻击。<br>这种攻击中，恶意数据不会接触到web服务器，它完全在客户端由JavaScript代码反映出来。


If the script is enclosed inside a <script> element, it won't be shown on the screen. 
