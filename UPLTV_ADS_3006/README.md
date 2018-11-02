# UPSDK 3006测试流程
date:2018.10.24
## 更新日志：
1.增加_NEW_SDK_INIT打点
2.新增视频联盟admob_new，可以配置多层，只有新版本（16.5.0+）支持
3.兼容Admob聚合和UPLTV聚合SDK的共存方案
新版支持：Facebook、IronSource
旧版支持：Vungle、UnityAD、Adcolony、Chartboost
4.聚合广告分海外、国内渠道分别打包（外部统计包请配合升级至3200版本）
5.升级adcolony到3.3.5
6.升级dap到1.2.0 + 1.0.8.5(去掉manifest中定制部分，加入海外默认联盟中)
7.实现facebook_bidding新逻辑
8.升级头条到1.9.6.2
bug：
1.部分联盟接入版本号显示不正确
2.素材上报只打开S3时不上报的问题

## 一、	广告测试内容
A.	国内国外是否包含正确的联盟
B.	国内和国外都正常显示广告包括
Banner
激励视频
插屏广告
C.	广告的回调是否正常
D.	Dap和Toutiao,adcoloy能否正常出广告

## 二、	统计上报的测试内容
A.	国内国外统计包的不同
国内取imei,androidid，国外不取imei和androidid

B.	打点能够正常上报，主要测试 NEW_SDK_INIT打点

## 三、	2中配置3个adomb_new联盟，且能出现两次不同key的广告，并回调正常
        
## 四、	3中对应不同的gms版本，只配置admob，看是否出诸如fb和unity的联盟
        在新版本(gms16.5.0)时候发现还出现unity
        
## 五、	统计包上报
A.接入是否有错误
B.打点是否正常
C.国内和国外包的区别

## 六、  adcolony 接入是否有问题，运行是否有error

## 七、  dap中去掉3005中dap_ads.aar是否可以播放广告

## 八、  facebook_bidding的功能是否被实现

## 九、  新版头条是否能播放

## 十、  查看bug是否被解决

