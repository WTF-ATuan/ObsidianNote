一位蓋住一位是

不是因為git的關係 而是因為策略的問題 
每個引擎策略都會不一樣

git flow
分支策略 
為什麼要開branch
分支永遠不會返回的 
最新的功能 再 develop 上

懂策略的人比較不會為了版本出去 而是為了功能
單元要多大，功能要多大，切得越少越好
feature(功能)
開出去的新branch 永遠不會消失 develop 線永遠不會往前
feature 線後面整合
一個功能要多大，要有共識
功能結束 才會 Merge 回到develop線上
以為功能很小 拆了feature 之後發現拆太大 又在往下拆 feature

怎麼知道做完了? 提早驗證 怎麼樣早點驗證? 
彼此都不知道彼此

做完的定義? 要一起達成共識
事前溝通不夠
什麼樣叫做完成的功能 
沒想到就沒想到，可以不用在同一個branch上做設定

規劃功能有問題

develop 線 做什麼功能後 都要跑回來

版本號 : https://zh.wikipedia.org/wiki/%E8%BB%9F%E4%BB%B6%E7%89%88%E6%9C%AC%E8%99%9F

git 分散式版本控制

revert => 捨去原本的commit (原本 add revert 就會 remove 掉)


---

Git 規格書
**Commit 記錄訊息最好兼俱 Why 及 What，讓日後進行維護人員更快進入狀況。**

基本動詞 
-   feat: 新增/修改功能 (feature)。
-   fix: 修補 bug (bug fix)。
-   remove : 移除(remove file)。
-   docs: 文件 (documentation)。
-   refactor: 重構 (既不是新增功能，也不是修補 bug 的程式碼變動)。
-   perf: 改善效能 (A code change that improves performance)。
-   test: 增加測試 (when adding missing tests)。
-   revert: 撤銷回覆先前的 commit 例如：revert: type(scope): subject (回覆版本：xxxx)。

我們想要什麼樣子 的commit 規格書?
Commit Message
範例 : 
<font color=red> " feat: "  </font>  <font color=yellow> "add Test - Should_Binding_Player_Events"</font>

動詞 + 對那樣東西做了什麼









