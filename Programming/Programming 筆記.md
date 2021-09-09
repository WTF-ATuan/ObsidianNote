
物件導向
單一職責!!

問題 : view 要如何發出Event 他們為什麼需要發送 event  
他為什麼要擁有 signal bus ? 他們需要EventStore? 

Aggregate 職責 : 產生事件 or 發送事件? 
Aggregate 需要自己發送事件嗎? 為什麼 ?'

UseCase 職責 : 如果 Aggregate 只負責產生事件，那usecase 的職責就是負責把事件傳出去

那在View 端 可以做到這個職責分層嗎?

---

目前重要的問題 : Domain 在 new 時 發出 Domain Event view component 都還來不及註冊view component ID ， domain Event 就已經發送完了，因此得到 null expenstion
以及 如果讓 domain 自行發送事件的話， 就必須得有signalbus 的存在
而signalbus 讓我很不方便測試

待作項目
1.  成功產生 domain Event  Y
2.  讓RotatePath的 constrostor 需要 ID 建置 Y (測試通過)
3.  成功發送 domain Event (測試保護) Y (沒辦法寫測試，因為環境不好模擬，他像是一個中繼站，應該可以測試 他的 前跟後， 如果都沒問題才會是他的問題)
4.  實作 Controller  Y
5.  現在問題 : Controller 已經成功發送 Event But Presenter  Y 
6.  使用 DomainEvent Store 去管理 domainEvent的 接收 Y
7.  View 端 發事件

---
舊版系統 如何以 id 進行呼叫 readModel

引擎驅動 ?  用view 去偵測 domain 
盡可能的方便測試 
collider 觸發?
這個Event 的目的是什麼?
如果發了Event 只有一個人收到，那為什麼不直接call他?
Collider 也是 Domain 
格鬥遊戲的collider 的 Domain

先求有再求好 
邊做邊重構
大可以一開始先全部寫在一起，之後再慢慢重構。
任何新功能 都是 prototype 

如何從咖哩自己煮 => 變成調理包 
量產你的產品?
獨立思考 
不教你釣魚，也不給你工具，要思考怎麼抓魚

只有程式量產，其他人或團隊or 設計 沒有跟上，那幫助也只是10% 這樣之後還是一樣要修改很多問題


為什麼要有 viewEventSubscribe? 
我希望不管是 domain or view Event 都不用去 擁有 presenter 或是controller 這類的 adpter 的實體，我希望她們最多就跟 signalBus 耦合就好了，我覺得這樣職責較輕也可以區分 事件是由哪裡發出的 domain 對 view => domain Event 
view 對 domain => view Event



