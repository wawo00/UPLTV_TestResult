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

### 加载到且能播放插屏广告
admob
applovin
ironsource
### bidding测试debug数据


{"__aff_info":"{\"aff_name\":\"facebook\",\"aff_key\":\"783955231747423_1064291897047087\",\"open_i_b\":1,\"aff_ttl\":1800}","is_ready":false,"price":0}
{"__aff_info":"{\"aff_name\":\"batmobi\",\"app_key\":\"T4E7MU69AU3R7JHUHSW5JYAJ\",\"placement_id\":\"15169_08173\",\"aff_ttl\":1800}","is_ready":true,"price":-1,"ad_token":"batmobi_15169_08173"}
{"__aff_info":"{\"aff_name\":\"mobpower\",\"app_key\":\"3fc7cbe75b45e7ce18b7f54b5edfda39\",\"app_id\":\"90002\",\"placement_id\":\"21408\",\"open_i_b\":0,\"aff_ttl\":1800}","is_ready":true,"price":-1,"ad_token":"mobpower_21408"}


[{"__aff_info":"{\"aff_name\":\"facebook\",\"aff_key\":\"783955231747423_1064291897047087\",\"open_i_b\":1,\"aff_ttl\":1800}",
"is_ready":false,"price":0,"ad_token":"facebook_rd_783955231747423_1064291897047087"},
{"__aff_info":"{\"aff_name\":\"batmobi\",\"app_key\":\"T4E7MU69AU3R7JHUHSW5JYAJ\",\"placement_id\":\"15169_08173\",\"aff_ttl\":1800}","is_ready":true,"price":-1,"ad_token":"batmobi_15169_08173"},
{"__aff_info":"{\"aff_name\":\"mobpower\",\"app_key\":\"3fc7cbe75b45e7ce18b7f54b5edfda39\",\"app_id\":\"90002\",\"placement_id\":\"21408\",\"open_i_b\":0,\"aff_ttl\":1800}","is_ready":true,"price":-1,"ad_token":"mobpower_21408"}]


["batmobi_15169_08173","mobpower_21408","facebook_rd_783955231747423_1064291897047087"]


mBiddingAffKeys=["batmobi_15169_08173","mobpower_21408","facebook_rd_783955231747423_1064291897047087"]


 if (firstKey.equals(affInfo.getPrimaryKey())) {
                                                    sLoadManager.doAfterBiddingComplete(firstKey, true);
                                                } else {
                                                    sLoadManager.doAfterBiddingComplete(firstKey, false); //batmobi_15169_08173
                                                }

 public void doAfterBiddingComplete(String key, boolean biddingSuccess) {  batmobi_15169_08173 false
        LogHelper.i("LoadManager " + key + " doAfterBiddingComplete with " + biddingSuccess);


BaseAdAdapter adAdapter = mCacheAds.get(key);
0 = {ConcurrentHashMap$MapEntry@6439} "toutiao_901121417" -> 
1 = {ConcurrentHashMap$MapEntry@6440} "facebook_rd_783955231747423_1064291897047087" -> 
2 = {ConcurrentHashMap$MapEntry@6441} "mobpower_21408" -> 
3 = {ConcurrentHashMap$MapEntry@6442} "batmobi_15169_08173" -> 
4 = {ConcurrentHashMap$MapEntry@6443} "batmobi_15169_04868" -> 
5 = {ConcurrentHashMap$MapEntry@6444} "dap_146386" -> 
 

 adAdapter.loadByBiddingComplete(biddingSuccess); -->load batmobiRewardAdapter


  if (!biddingSuccess) {
            mLoadingAds.remove(key);  //remove batmobi_15169_08173
    }
 I/AdsSdk_3006.0: cplog: 视频广告展示,联盟：batmobi       




### 问题：
#### 有些联盟没有提供
vk
batmobi
inmobi
vungle

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
暂时没有@王涛

#### 展示的log只有一个
AdsSdk_3006.0: BannerAdapter isValid: false
AdsSdk_3006.0: BannerAd: banner_aaa: only_wifi：false，netType: wifi
AdsSdk_3006.0: BannerAd: banner_aaa: 展示联盟：admob
AdsSdk_3006.0: BannerAd: banner_aaa: 可以显示，设置视图可见
AdsSdk_3006.0: banner ====>exist cpPlaceId:banner_aaa,exist: true

#### cocoscpp，cocoslua，cocosjs中不应该包含youlan
#### dap的版本号显示为unknown，可以见图片dap_version_unknow

#### 错误信息：

##### A.admob banner

 onError admob, message is AdmobBannerAdapter failed with code: 3

