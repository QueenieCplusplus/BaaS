# BaaS

BaaS, backend as a service since 2016 &amp; amateur in 2018.

https://pattyappier.blog/2019/01/17/cloud-sql/

https://pattyappier.blog/2019/01/17/cloud-datastore-應用程式非關聯性式儲存機制/

FB 收購 Parse 不做對外服務，而是內化予內部應用; Googls 收購 Firebase 作為對外的 BaaS 服務。從 2016 年 I/O 大會起，直至 2018 年，歷經兩年，方才成熟穩定，目前慢慢追加擴充功能。

Firebase from GCP https://console.firebase.google.com/?pli=1 

StackMob https://www.spigotmc.org/resources/stackmob-enhance-your-servers-performance.29999/

Parse from FB https://parseplatform.org 

# Background

* 人力成本：

      行動應用的製作成本是非常高的，基於團隊人才需要包含 UI、iOS、Android、Backend、DB、Frontend 之外，手機系統本身也擁有其複雜程度和難以預料的意外狀況。

* 網路不穩：

      不同於 Web app 的 always on line，手機的網路是行進中的網路，傳輸資料的品質不容易控制。

* 行動後端：

      目前 GCP、AWS、Azure 基於後端開發的思考，從 web js 衍生出對行動應用的 iOS/Android 的應用設計。

* 集成服務：

      BaaS服務提供商的基礎服務是數據/文件存儲，主要幫助 App 開發者解決存儲的問題。更進一步的集成服務則包括：帳戶驗證管理、遠端消息推送推播、廣告推薦等。

# API & SDK

BaaS分兩種模式：一種是API模式，讓開發者自己拓展代碼；另一種是SDK模式，提供如iOS、Android及Windows Phone等的SDK。

# Reused Features

* offline cache, 離線快取或是離線資料庫 （筆者尚未研究）

* login auth, 登入驗證

* cloud message (remote notification), 遠(雲)端推播
  筆者於2018年使用過。

* realtime DB, 即時資料庫 

* users behavior analytics, 使用者行為分析


# Extension

* adMob, 應用程式內廣告，安裝與設定廣告。

* invents, 一種以使用者拉使用者的一種機制，不同的社群間推廣。

* A/B testing, 持續應用體驗, 利用 remote config, 不改原有代碼，完成測試。

       其他類似的應用尚有 Performance Monitor（針對國家地區對畫面和網路做效能分析）、Test Lab（自動化測試工具）。
       //

* Cloud Firestore, 雲端資料庫：

   https://pattyappier.blog/2019/01/17/cloud-sql/

    支援更多資料格式，例如 geopint、reference。
 
    支持鍵值對的索引，例如 sort、compound、filter。
 
    負載不足，會自動擴展。
  
    限制：因為與 Realtime DB 的 Firebase 架構不同，故兩者無法轉換。
     //

* crashlytics, 閃退分析器：

  ios: pod 'Crashlytics', '~>3.9.3"

  android: implementation 'com.crashlytics.sdk.android:crashlytics:2.9.3"
    
# Feature for Web 

* Host, 靜態網頁頁面來源:

      當需要用到固定資料，或單純利用 Http Requst 存取 Restful Api 時，由於 Open Data 常常放入我們開發者不需要的資訊，增加煩擾不便，故此網站伺服器功能，能提供靜態網頁，穩定的頁面來源，提供手機做資料來源的媒介。

* App Index, SEO 應用程式推廣

* Dynamic Links, 深度動態連結：

      適合 web app + mobile app 一起使用，細部筆者尚需研究。

# Share Resources 

 * Cassandra (Column-oriented)
 
   https://github.com/QueenieCplusplus/DataMining_Cassandra
 
 * Redis (k/V-oriented)

 * MongoDB (Doc-oriented)
 
 * CouchDB (Doc-oriented) 筆者尚未研究
 
 * Dynamo DB (k/V-oriented) 筆者尚未研究




