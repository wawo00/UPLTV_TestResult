## UPLTV ADS 3006 国际版

### 测试参数
包名：
roy.wan.foreign


广告配置：
http://test-ads-sdk.avidly.com/?__pkg=roy.wan.foreign&__os=android&country=DEFAULT&encrypt=1

设备信息：
nexus5
Android 6.0.1

### 加载到且能播放banner广告
admob

### 加载到且能播放视频广告：
adcolony
applovin
appnext
ironsource
mobvista
unity
vungle

### 加载到且能播放激励视频
admob
applovin
ironsource
vungle
 


### 问题：
#### 有些联盟没有提供
vk
batmobi
inmobi

#### tapjoy这个联盟有时候会播放完视频后自己关闭且没有回调

#### onAdOpened 和 onAdClosed数目不等
 IronSource: onAdClosed() with type RewardedVideo 
 ironsource_0 onAdClosed 
 unity_rewardedVideo onAdClosed 
 IronSource: onAdClosed() with type RewardedVideo 
 ironsource_0 onAdClosed 
 unity_rewardedVideo onAdClosed 
 admob_ca-app-pub-9986066456792135/1606720605 onAdClosed 
applovin_92ec4538b2029e4d onAdClosed 
IronSource: onAdClosed() with type Interstitial 
ironsource_i_0 onAdClosed 
vungle_INTERST54803 onAdClosed 


 unity_rewardedVideo onAdOpened 
 ironsource_0 onAdOpened 
 unity_rewardedVideo onAdOpened 
 admob_ca-app-pub-9986066456792135/1606720605 onAdOpened 
 applovin_92ec4538b2029e4d onAdOpened 
 ironsource_i_0 onAdOpened 
 vungle_INTERST54803 onAdOpened 

#### 使用log中什么来确定广告播放完后发送了奖励

#### 展示的log只有一个
AdsSdk_3006.0: BannerAdapter isValid: false
AdsSdk_3006.0: BannerAd: banner_aaa: only_wifi：false，netType: wifi
AdsSdk_3006.0: BannerAd: banner_aaa: 展示联盟：admob
AdsSdk_3006.0: BannerAd: banner_aaa: 可以显示，设置视图可见
AdsSdk_3006.0: banner ====>exist cpPlaceId:banner_aaa,exist: true

#### 暂时没有找到NEW_SDK_INIT打点


#### 错误信息：

##### A.admob banner

 onError admob, message is AdmobBannerAdapter failed with code: 3

