我不想讓 Path : Mono 這個腳本餐與其他物件的生成
以及我不想讓他發事件出去，因為這樣他的職責太多了
我希望他可以執行發派的工作以及表演就好

以及 Character : Mono 這個腳本餐與行為的生成
以及發事件，我不想要他有signalBus

IoC 控制反轉

unity 的getcomponent 可以 get到 interface 他給了unity gameobject 身上有的東西

我可以設計一個interface builder 給他 物件ID以及資料ID
他回傳給我一個interface 而interface builder 就可以用as single 的方式去實作他


behavior 該做什麼?  feature?
character 該做什麼? feature?

最初的目的behvior 可以控制角色移動 以及播放動畫 
所以 behavior 可以控制Character?
所以可以理解成 behavior 發出指令讓角色撥放動畫?

character 只是一個中心指揮官 他啥都不會做


目的 : 我給角色 ID 以及 Data ID 給我的API  我的API 會直接回傳給我相對應的interface，在這個API上面設計卡住了 因為zenject的實作不太了解這個設計原則

每個接口都有實例 










