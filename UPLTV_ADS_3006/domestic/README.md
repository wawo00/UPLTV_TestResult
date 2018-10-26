## UPLTV ADS 3006 国内版

### 测试参数
包名：roy.wan.inland
广告配置：http://test-ads-sdk.avidly.com/?__pkg=roy.wan.inland&__os=android&country=DEFAULT&encrypt=1
设备信息：nexus5 Android 6.0.1

### 加载到且能播放视频广告：
 centrixlink  
 oneway  
 vungle_DEFAULT99486  
 toutiao_901121365  
 chartboost_reward 
 


### 问题：
#### onAdOpened 和 onAdClosed数目不等
 [ALL] 10-25 11:28:07.752  9734  9734 I AdsSdk_3006.0: UPRewardVideoWrapper onAdOpened 
 [ALL] 10-25 11:37:02.093 13566 13566 I AdsSdk_3006.0: centrixlink onAdOpened 
 [ALL] 10-25 11:38:13.498 13566 13566 I AdsSdk_3006.0: chartboost_reward onAdOpened 
 [ALL] 10-25 11:39:17.908 13566 13566 I AdsSdk_3006.0: oneway onAdOpened 
 [ALL] 10-25 11:40:58.747 13566 13566 I AdsSdk_3006.0: vungle_DEFAULT99486 onAdOpened 
 [ALL] 10-25 11:42:02.646 13566 13566 I AdsSdk_3006.0: toutiao_901121365 onAdOpened 
 [ALL] 10-25 11:44:24.786 13566 13566 I AdsSdk_3006.0: centrixlink onAdOpened 
 [ALL] 10-25 11:45:02.424 13566 13566 I AdsSdk_3006.0: chartboost_reward onAdOpened 
 [ALL] 10-25 11:45:43.258 13566 13566 I AdsSdk_3006.0: oneway onAdOpened 

 [ALL] 10-25 11:38:07.696 13566 13566 I AdsSdk_3006.0: centrixlink onAdClosed 
 [ALL] 10-25 11:39:04.934 13566 13566 I AdsSdk_3006.0: chartboost_reward onAdClosed 
 [ALL] 10-25 11:40:53.093 13566 13566 I AdsSdk_3006.0: oneway onAdClosed 
 [ALL] 10-25 11:41:51.206 13566 13566 I AdsSdk_3006.0: vungle_DEFAULT99486 onAdClosed 
 [ALL] 10-25 11:44:56.931 13566 13566 I AdsSdk_3006.0: centrixlink onAdClosed 
 [ALL] 10-25 11:45:25.899 13566 13566 I AdsSdk_3006.0: chartboost_reward onAdClosed 

#### 展示的log只有一个
 Centrixlink: adEventReport: AD_EVENT_TYPE_CallHasPreloadSuccess
 AdsSdk_3006.0: cplog: 视频广告 isReady return true
 AdsSdk_3006.0: cplog: 视频广告展示,联盟：centrixlink
 Centrixlink: adEventReport: AD_EVENT_TYPE_CallHasPreloadSuccess
 AdsSdk_3006.0: Adapter: REWARDVIDEO centrixlink isValid: true

#### 暂时没有找到NEW_SDK_INIT打点


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
