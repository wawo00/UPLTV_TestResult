## UPLTV ADS 3006 国内版

### 测试参数
包名：
roy.wan.inland

广告配置：
http://test-ads-sdk.avidly.com/?__pkg=roy.wan.inland&__os=android&country=DEFAULT&encrypt=1


设备信息：
nexus5 
Android 6.0.1

### 加载到且能播放视频广告：
 centrixlink  
 oneway  
 vungle_DEFAULT99486  
 toutiao_901121365  
 chartboost_reward 
 
### 统计包打点
 同意授权

 I/<ALY Android>_3200: logEvent key: _NEW_SDK_INIT, value: [{__language=en_US, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=f8bad30d359540b685486a5694a8a90b, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __open_id=1dc3cbd87a22a2e544febca17ba257c3, __ver_name=3.0.0.6, __device_id=352136064190941}]


I/<ALY Android>_3200: logEvent key: _NEW_CFG_DLDOK, value: [{__language=en_US, __location=CN, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=f8bad30d359540b685486a5694a8a90b, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __config_ver=47, __open_id=1dc3cbd87a22a2e544febca17ba257c3, __ver_name=3.0.0.6, __device_id=352136064190941, __count=0}]


不同意授权

 I/<ALY Android>_3200: logEvent key: _NEW_SDK_INIT, value: [{__language=en_US, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=aaf47fb409f3472d86e47903873c9dfb, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __open_id=ec395b8d091f6c323e360dd2574208c9, __ver_name=3.0.0.6, __device_id=}]

 I/<ALY Android>_3200: logEvent key: _NEW_CFG_DLDOK, value: [{__language=en_US, __location=CN, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=aaf47fb409f3472d86e47903873c9dfb, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __config_ver=47, __open_id=ec395b8d091f6c323e360dd2574208c9, __ver_name=3.0.0.6, __device_id=, __count=0}]


### 问题：
#### onAdOpened 和 onAdClosed数目不等
 onAdOpened：
 UPRewardVideoWrapper  
 centrixlink  
 chartboost_reward  
 oneway  
 vungle_DEFAULT99486  
 toutiao_901121365  
 centrixlink  
 chartboost_reward  
 oneway 

onAdClosed ：
 centrixlink  
 chartboost_reward  
 oneway  
 vungle_DEFAULT99486  
 centrixlink  
 chartboost_reward  

#### 展示的log只有一个
 Centrixlink: adEventReport: AD_EVENT_TYPE_CallHasPreloadSuccess
 AdsSdk_3006.0: cplog: 视频广告 isReady return true
 AdsSdk_3006.0: cplog: 视频广告展示,联盟：centrixlink
 Centrixlink: adEventReport: AD_EVENT_TYPE_CallHasPreloadSuccess
 AdsSdk_3006.0: Adapter: REWARDVIDEO centrixlink isValid: true




#### 错误信息：

##### A.头条

 java.lang.SecurityException: "passive" location provider requires ACCESS_FINE_LOCATION permission.
at android.os.Parcel.readException(Parcel.java:1620)
at android.os.Parcel.readException(Parcel.java:1573)
at android.location.ILocationManager$Stub$Proxy.requestLocationUpdates(ILocationManager.java:606)
at android.location.LocationManager.requestLocationUpdates(LocationManager.java:880)
at android.location.LocationManager.requestSingleUpdate(LocationManager.java:688)
at com.bytedance.sdk.openadsdk.g.b.b(AdLocationUtils.java:169)
at com.bytedance.sdk.openadsdk.g.b.d(AdLocationUtils.java:96)
at com.bytedance.sdk.openadsdk.g.b.a(AdLocationUtils.java:38)
at com.bytedance.sdk.openadsdk.activity.TTRewardVideoActivity.k(TTRewardVideoActivity.java:288)
at com.bytedance.sdk.openadsdk.activity.TTRewardVideoActivity.j(TTRewardVideoActivity.java:264)
at com.bytedance.sdk.openadsdk.activity.TTRewardVideoActivity.d(TTRewardVideoActivity.java:47)
at com.bytedance.sdk.openadsdk.activity.TTRewardVideoActivity$4.a(TTRewardVideoActivity.java:206)
at com.bytedance.sdk.openadsdk.core.video.a.a.b(BaseVideoController.java:313)
at com.bytedance.sdk.openadsdk.core.video.a.a.a(BaseVideoController.java:480)
at com.bytedance.sdk.openadsdk.g.y.handleMessage(WeakHandler.java:30)
at android.os.Handler.dispatchMessage(Handler.java:102)
at android.os.Looper.loop(Looper.java:148)
at android.app.ActivityThread.main(ActivityThread.java:5417)
at java.lang.reflect.Method.invoke(Native Method)
at com.android.internal.os.ZygoteInit$MethodAndArgsCaller.run(ZygoteInit.java:726)
at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:616)

##### B.centrixlink 
 java.lang.NoSuchFieldException: No field mProxyContext in class Landroid/media/MediaPlayer; (declaration of 'android.media.MediaPlayer' appears in /system/framework/
 	at java.lang.Class.getDeclaredField(Native Method)
 	at com.centrixlink.SDK.FullScreenVideoFragment.g(Unknown Source)
 	at com.centrixlink.SDK.FullScreenVideoFragment.f(Unknown Source)
 	at com.centrixlink.SDK.FullScreenVideoFragment.onCompletion(Unknown Source)
 	at android.widget.VideoView$3.onCompletion(VideoView.java:483)
 	at android.media.MediaPlayer$EventHandler.handleMessage(MediaPlayer.java:2820)
 	at android.os.Handler.dispatchMessage(Handler.java:102)
 	at android.os.Looper.loop(Looper.java:148)
 	at android.app.ActivityThread.main(ActivityThread.java:5417)
 	at java.lang.reflect.Method.invoke(Native Method)
 	at com.android.internal.os.ZygoteInit$MethodAndArgsCaller.run(ZygoteInit.java:726)
 	at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:616)
