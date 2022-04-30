# jdckWebApp   


###   紧急 :warning:  :warning:  :warning: ：  
>**请2022-04-24之前有提交到我仓库Pull Request,并且里面包含公网服务器IP、用户名、密码等隐私数据的，立即修改密码、重置token。目前仓库已经重新清空并禁止了Pull Request，但是如果清空之前Pull Request有被其他人看到，那么你服务器的CK有泄露风险。**


###   最后申明一下，APP没有做加密处理，有被反编译的风险，大家传播使用时需谨慎！！




#### 介绍
使用内置浏览器登录京东后，获取CK
     

>#### 注意 
> apk存在被反编译，配置参数泄露的危险，传播时请慎重！！！

#### 更新
- 2022-4-26：
    改了几个Bug：  
        ① 青龙的版本号对比问题；  
        ② 旧版青龙的_id数据类型问题；  
        ③ 修改了Issue#I54O20，没复现问题，也不知道改的有没效果；  

- 2022-4-25：
    - APP 1.1.1版本,更新内容如下：    
            ① APP的界面整体换了下，不然感觉有点掉链子，虽然本来就是就是写来玩的。  
            ② 浏览器添加了无痕/标准切换功能，终于不用装一堆APP来维护账号了。  
            ③ 添加青龙面板的环境变量维护功能（新增、修改、查看、启用、禁用），可以打包APP的时候内置青龙服务器参数，也可以在使用的时候配置。  
            ④ CK提交的时候，默认提交到青龙服务器，没有配置青龙服务器，则提交到GitEE。  
            ⑤ 添加浏览器默认的首页地址设置功能（之前有评论提到京东健康的，满足你了）。    
            ⑥ 添加APP功能权限，区分管理员（所有功能）和普通用户（没有青龙服务器维护功能）。  
        
        打包配置：    
            [config.gradle](https://gitee.com/maxinDev/jdck-web-app/blob/master/config.gradle)  中配置打包的内置参数；  
            [app/build.gradle](https://gitee.com/maxinDev/jdck-web-app/blob/master/app/build.gradle) 中配置APP功能权限，默认管理员。

- 2022-4-21 ~ 2022-4-22：
     -  dev分支已完成 提交CK到青龙，以及青龙的登录、环境变量维护功能，已使用2.11.3版本测试通过。  

     -  新增**青龙脚本** [giteeCK-a3.py](https://gitee.com/maxinDev/jdck-web-app/blob/master/temp/giteeCK-a3.py)   
        添加环境变量【gitee_ck_certificate】，脚本自动读取配置在环境变量中的参数,  
        格式是：gitee私人令牌@giteeIssue浏览器地址@青龙服务器IP',  
        示例：d05279c13bb31234567898092@https://gitee.com/maxinCom/jdcookie-nice/issues/I65I0U@http://127.0.0.1:5700'  

           


- 2022-4-20：
     -  捣鼓了下QQ授权登录，比较鸡肋，需要把APP设置成默认浏览器，具体看下面的使用说明。

- 2022-4-19：
     -  **青龙脚本兼容版**  [giteeCK.py](https://gitee.com/maxinDev/jdck-web-app/blob/master/temp/giteeCK.py) ,已测试 2.8.0 、2.11.2

- 2022-4-18：
    - 解决android12安装出现-22问题
    - 脚本添加推送

    
#### 后续的一些想法❌✔：

- 2022-4-22：
    - ✔ 区分管理员、普通用户APP，管理员可登录、维护青龙数据， 普通用户只能使用浏览器抓CK，以及提交到GitEE或青龙服务器。
- 2022-4-19：
    - ✔ APP添加青龙IP的配置页面，有公网的可以直接提交CK到服务器，免得嫖Gitee服务器；
    - ✔ APP接入青龙的一些简单功能，暂时接入（登录、环境变量维护）；
    

#### 

#### 安装教程


#### 使用说明


- QQ授权登录


    > 偶然发现浏览器在JD登录页有个QQ授权登录，可以拉起手机QQ授权，于是捣鼓了一下，发现如果在【JdWeb】APP中使用QQ授权登录，QQ授权后，会跳转到手机的默认浏览器；
    > 额。。？这样我没办法拿到CK了啊。。 最后妥协了，直接在手机 设置 -> 应用管理 -> 默认应用管理 -> 浏览器  ，把【JdWeb】APP设置成了默认浏览器，再测试了一次，发现成功了。
    > 总的看起来，非常鸡肋。聊胜于无吧，先记录下。


#### 参与贡献

1.  Fork 本仓库
2.  新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request

