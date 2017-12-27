# npm-library
npm的网络代理和淘宝镜像的设置


---

##一，网络代理设置
###（一）添加代理
**npm config set proxy http://serverId:port**

###（二）添加https代理
**npm config set https-proxy http://serverId:port**


###（三）添加需要验证的代理
**npm config set proxy http://username:possword@serverId:port**
**npm config set https-proxy http://username:possword@serverId:port**
###如果代理不支持https的话需要修改npm存放package的网站地址。
**npm config set registry "http://registry.npmjs.org/"**

##（四）taobao镜像设置
###1.临时使用
**npm --registry https://registry.npm.taobao.org install express**

###2.永久使用，方法一
**npm install -g cnpm --registry=https://registry.npm.taobao.org**

###3.永久使用，方法二
（建议使用-[它是只修改npm的registry配置，并不像2中一样下载cnpm这个项目]）
**npm config set registry https://registry.npm.taobao.org**

*注意*
*检验是否安装成功：*
（指的是永久型方法一）
cnpm config get registry 或  cnpm info express/other packageName
（指的是永久型方法二）
npm config get registry  或  npm info express/other packageName

###4.使用方法
（4.2指的是永久型方法一）
**cnpm install packageName**
（4.2指的是永久型方法二）
**npm install packageName**



