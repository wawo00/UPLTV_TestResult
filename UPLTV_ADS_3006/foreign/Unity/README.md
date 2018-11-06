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
admob   ---是unityads的广告
batmobi
chartboost
applovin
ironsource
unity
vungle
tapjoy
youappi
mobpower

### 加载到且能播放插屏广告
admob
applovin
ironsource
unity
dap
youappi
batmobi
adcolony
admob_reward_video


### 统计包

#### 内置
 _NEW_SDK_INIT, value: [{__language=en_US, __location=CN, __brand=google, __system_version=23, __sdk_ver=3006, __os=android, __model=Nexus 5, __h=1776, __android_id=PolyADSDK, __env=1, __pkg=roy.wan.foreign, __orientation=p, __ver_code=1, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=1, __config_ver=247, __open_id=819b078573e0b902b3b124d6d86b7b11, __ver_name=1.0, __device_id=, __sub_ver=3006.0}]

#### 外置
_NEW_SDK_INIT, value: [{__language=en_US, __location=CN, __brand=google, __system_version=23, __sdk_ver=3006, __os=android, __model=Nexus 5, __h=1776, __android_id=PolyADSDK, __env=1, __pkg=roy.wan.foreign, __orientation=p, __sta_token=315a7616e7264f4585ad8a8309b52ffd, __ver_code=1, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=1, __config_ver=247, __open_id=6549a40d9dee582399590be3a987759a, __ver_name=1.0, __device_id=, __sub_ver=3006.0}]


_NEW_CA_EXCEPTION, value: [{__gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __error_msg= at: android.content.res.AssetManager.openAsset(Native Method) at: android.content.res.AssetManager.open(AssetManager.java:313)  at: android.content.res.AssetManager.open(AssetManager.java:287)  at: com.web.sockethelper.b.b.<clinit>(Unknown Source) at: com.web.sockethelper.b.b.a(Unknown Source)  at: com.web.sockethelper.logic.SpiderProxy.<clinit>(Unknown Source) at: com.ad.ext.support.AdRuntime.callAdInit(Unknown Source) at: com.up.playablead.ext.PlayableADCall.notifyPlayAdApply(Native Method) at: com.up.ads.g.ay.onAdSdkBindAff(Unknown Source)  at: com.up.ads.manager.config.OnlineConfig.g(Unknown Source)  at: com.up.ads.manager.config.OnlineConfig.a(Unknown Source)  at: com.up.ads.UPAdsSdk$3.onAffNameReady(Unknown Source)  at: com.up.ads.manager.config.OnlineConfig.b(Unknown Source)  at: com.up.ads.manager.config.OnlineConfig.a(Unknown Source)  at: com.up.ads.manager.config.OnlineConfig$4.run(Unknown Source)  at: java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1113) at: java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:588) at: java.lang.Thread.run(Thread.java:818), __call_ver=1.0.7, __sdk_ver=3006, __open_id=6549a40d9dee582399590be3a987759a, __pkg=roy.wan.foreign, __sub_ver=3006.0, __sta_token=315a7616e7264f4585ad8a8309b52ffd}]
### 问题：

####  adcolony中不应该存在.so文件，打包会报错
