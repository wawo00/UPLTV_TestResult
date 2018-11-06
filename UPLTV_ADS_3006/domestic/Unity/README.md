## UPLTV ADS Unity3006 国内版

### 测试参数
包名：
roy.wan.inland

广告配置：
http://test-ads-sdk.avidly.com/?__pkg=roy.wan.inland&__os=android&country=DEFAULT&encrypt=1


设备信息：
nexus5 
Android 6.0.1

### 加载到且能播放视频广告：
 oneway  
 vungle_DEFAULT99486  
 toutiao_901121365  
 
### 统计包打点

#### 内置统计包：


 同意授权


 ===> xxx customerid: PolyADSDK
 ===> xxx customerid: PolyADSDK
 ===> xxx disableAccessPrivacyInfo: false
 ===> xxx disableAccessPrivacyInfo: false
 tryExeQueryRequest, userid，未获取
 ====> xxx, deviceid:68cfc7bb674f7b7f_352136064190941_
 ====> xxx, deviceid:68cfc7bb674f7b7f_352136064190941_
 ====> xxx, openid:80b62288b18854cd28d2edff45ce7262
 ====> xxx, openid:80b62288b18854cd28d2edff45ce7262
 ====> xxx, gaid:
 ====> xxx, gaid:
 ====> xxx, disable:false


 I/<ALY Android>_3200: logEvent key: _NEW_SDK_INIT, value: [{__language=en_US, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=f8bad30d359540b685486a5694a8a90b, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __open_id=1dc3cbd87a22a2e544febca17ba257c3, __ver_name=3.0.0.6, __device_id=352136064190941}]


I/<ALY Android>_3200: logEvent key: _NEW_CFG_DLDOK, value: [{__language=en_US, __location=CN, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=f8bad30d359540b685486a5694a8a90b, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __config_ver=47, __open_id=1dc3cbd87a22a2e544febca17ba257c3, __ver_name=3.0.0.6, __device_id=352136064190941, __count=0}]


不同意授权

 I/<ALY Android>_3200: logEvent key: _NEW_SDK_INIT, value: [{__language=en_US, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=aaf47fb409f3472d86e47903873c9dfb, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __open_id=ec395b8d091f6c323e360dd2574208c9, __ver_name=3.0.0.6, __device_id=}]

 I/<ALY Android>_3200: logEvent key: _NEW_CFG_DLDOK, value: [{__language=en_US, __location=CN, __brand=google, __system_version=23, __sdk_ver=3006.0, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=aaf47fb409f3472d86e47903873c9dfb, __ver_code=3006, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=0, __config_ver=47, __open_id=ec395b8d091f6c323e360dd2574208c9, __ver_name=3.0.0.6, __device_id=, __count=0}]


详情见 UPSDK3006_unity_domesic_ALY.txt


#### 外置统计包

_NEW_SDK_INIT, value: [{__language=en_US, __location=CN, __brand=google, __system_version=23, __sdk_ver=3006, __os=android, __model=Nexus 5, __h=1776, __android_id=68cfc7bb674f7b7f, __env=1, __pkg=roy.wan.inland, __orientation=p, __sta_token=eadee61de3a34fed97c2dbbc6240030b, __ver_code=1, __gaid=5a862c88-d254-45bc-be40-20af7d04b1b9, __w=1080, __install_fb=1, __config_ver=52, __open_id=7a511efa4eabd7f32f80c8a6717fc565, __ver_name=1.0, __device_id=352136064190941, __sub_ver=3006.0}]



详情见 UPSDK3006_unity_domesic_outer_ALY.txt

### 问题：


#### 会请求三个权限，获得用户电话，获得文件管理，获得定位信息
  <uses-permission
      name='android.permission.READ_PHONE_STATE'>
  </uses-permission>


  <uses-permission
      name='android.permission.INTERNET'>
  </uses-permission>
  <uses-permission
      name='android.permission.READ_EXTERNAL_STORAGE'>
  </uses-permission>

  <uses-permission
      name='android.permission.ACCESS_NETWORK_STATE'>
  </uses-permission>
  <uses-permission
      name='android.permission.READ_PHONE_STATE'>
  </uses-permission>
  <uses-permission
      name='android.permission.WRITE_EXTERNAL_STORAGE'>
  </uses-permission>

  <uses-permission
      name='android.permission.ACCESS_COARSE_LOCATION'>
  </uses-permission>

#### 既然不需要手动修改包名了，头条是否需要包含在提供的包中，不单独出包

#### mobvista加载不到：

11-06 11:23:05.626 2986-3225/? W/AdsSdk_3006.0: LoadManager mobvista_18188 removeLoading timeout
11-06 11:23:06.815 2986-3225/? W/AdsSdk_3006.0: LoadManager playableads_il-100013-1503555086979 removeLoading timeout

#### 错误信息：
无