# VPN
This project is to tell you how to create VPN  
首先要拥有一台国外服务器，建议购买Digitalocean的，DigitalOcean,具体方法我这里不在重复造轮子，详见从零开始，搭建属于自己的VPN。在这里补充几点，
1. 关于费用、优惠：要是学生的话，可以通过Github学生认证（链接https://education.github.com/pack）得到50美元的优惠。（要用自己的学校邮箱） 
DigitalOcean上最基础的服务器配置如下：每月5美元，1000GB流量，512MB的CPU，20G的SSD硬盘。完成DigitalOcean的注册后需要充值5美元激活账号，
这时需要有国外的信用卡或者使用PayPal，注册PayPal后绑定银联的银行卡就行，付费时直接从银行卡中扣费。（PayPal相当于国外的支付宝，也是很方便）。
2. 关于博客中pip安装改正原博主的：事实证明并不能用，不信可以自己去试试坑哦
下面是自己亲身实验成功的安装方法
$ sudo apt-get install python-pip python-dev build-essential$ sudo pip install --upgrade pip$ sudo pip install --upgrade virtualenv1233.
关于Shadowsocks安装，用下面的即可，不会出现其他问题pip install shadowsocks124.关于SSH Keys要在Windows上创建和使用SSH密钥，
您需要下载并安装PuTTY（用于通过SSH连接到远程服务器的实用程序）和PuTTYgen（用于创建SSH密钥的实用程序）。在PuTTY网站上，
在MSI（’Windows Installer’）下的页面顶部.msi的Package files部分下载该文件。接下来，通过双击并使用安装向导将其安装在本地计算机上。
安装程序后，通过“开始”菜单或点击Windows键并键入来启动PuTTYgen程序puttygen。密钥生成程序看起来类似于：如果您愿意，可以在底部自定义参数，
但在大多数情况下默认值是合适的。准备好后，单击右侧的“ 生成”按钮。系统可能会提示您“通过将鼠标移到空白区域上来生成一些随机性”。这种随机性，称为熵，
用于以安全的方式创建密钥，以便其他人无法再现它们。生成密钥后，您将看到文本框中显示的公钥。如果您计划将其添加到DigitalOcean帐户或服务器，
请将其复制到剪贴板中。请务必在文本区域内滚动，以便复制整个密钥。单击“ 保存私钥”按钮，然后选择一个安全位置以保留它。您可以随意命名您的密钥，
并.ppk自动添加扩展程序。使用PuTTY的公钥格式 您也可以单击“ 保存公钥 ”，但请注意：PuTTYGen保存公钥时使用的格式与authorized_keysLinux服务器上
用于SSH密钥身份验证的OpenSSH 文件不兼容。如果您需要在保存私钥后以正确的格式查看公钥，请执行以下操作之一：*单击“ 加载”按钮*导航到私钥并打开它。
公钥将再次重新显示。现在，您已将生成的密钥对保存在计算机上并可以使用，您可以：*将您的公钥添加到您的DigitalOcean帐户，以便能够在创建时将其嵌入到新
的Droplet中。*将您的公钥添加到现有Droplet以使用SSH密钥身份验证登录它们。
5.关于Shadowsocks客户端下载，这个客户端没有官网之类的，到GitHub下载即可https://github.com/shadowsocks/shadowsocks设置，现在打开谷歌试一下吧！
