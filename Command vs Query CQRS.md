Command(指令) 是會修改系統狀態但不回傳資料的操作

Query 是不會改變系統狀態但是會回傳資料的操作

**Command query responsibility segregation (CQRS)**

理想 Feature
**套用CQRS之後理想狀況是所有的Command共用相同的Output、Presenter以及View Model**

進階的 CQRS 系統可能會針對您的更新資料庫實作[事件溯源 (Event Sourcing，ES)](https://martinfowler.com/eaaDev/EventSourcing.html)，因此您只會在領域模型中儲存事件，而不會儲存目前的狀態資料。

同一份資料，有可能會有很多不同的呈現方式
EX : 主資料為 User 
有些人只要知道是ID 就好，但有些人需要知道更多數據
