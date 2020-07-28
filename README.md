# glados-checkin
  每天自动签到（天数+=1），使用Server酱推送结果到微信

# Server酱：
负责推送消息到微信。

[点此查看详情](http://sc.ftqq.com/3.version)


# Github Actions说明
## 一、Fork此仓库
![](http://tu.yaohuo.me/imgs/2020/06/f059fe73afb4ef5f.png)
## 二、设置账号密码

添加名为——值分别为：  
**SERVE**  ——**on/off** 你想你的serve酱开不开启通知  
**SCKEY**  ——**sckey**  开的话填你的serve酱的sckey，不开就不填   
**COOKIE** —— **cookie** 弄上你账号的cookie  

![](http://tu.yaohuo.me/imgs/2020/06/748bf9c0ca6143cd.png)

## 三、启用Action
1 点击**Action**，再点击**I understand my workflows, go ahead and enable them**  
2 修改任意文件后提交一次  
![](http://tu.yaohuo.me/imgs/2020/06/34ca160c972b9927.png)

## 四、查看运行结果
Actions > Cloud189Checkin > build  
能看到如下图所示，表示成功，或者看你微信通知  
![](http://tu.yaohuo.me/imgs/2020/06/289432b53bded61c.png)  

# 修改签到时间
可以在[.github/workflows/python-publish.yml]中修改  
```
on:
  schedule:
    - cron cron表达式
```
`0 9 * * * ` 表示每天9点启动，在GitHub的编辑页面中会有如下提示
![](https://raw.githubusercontent.com/458744230/pic/master/img/20200727230953.png)

注意时间是UTC时间，如果你在东八区，9表示每天9+8=17点签到

# 获取Cookies

以chrome为例

登录到web端,打开F12，依次点击Application，Cookies以查看所有的cookies，编辑取消所有的HttpOnly

![](https://cdn.jsdelivr.net/gh/458744230/pic/img/20200728205916.png)

然后再console界面输入document.cookie，就能获得文本形式所有的cookie，注意不带引号



# Reference

[glados-checkin](https://github.com/xiaomustudent/glados-checkin)

[GLaDOS](https://github.com/glados-network/GLaDOS)

