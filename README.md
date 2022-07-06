# leave-sample
一、說明

在《DDD實戰課》專欄第18節中我們用事件風暴完成了「在線請假考勤」項目的領域建模和微服務設計。
我們一起從程序員的視角去看看用DDD方法設計和開發出來的微服務代碼到底是什麼樣的？

二、項目回顧

「在線請假考勤」項目中，請假的核心業務流程是：「請假人填寫請假單提交審批。根據請假人身份、請假類型和請假天數進行校驗並確定審批規則。根據審批規則確定審批人，逐級提交上級審批，逐級核批通過則完成審批，否則審批不通過則退回申請人。」

本部分是請假微服務的示例代碼，採用的開發語言和數據庫分別是：Java、Spring boot和PostgreSQL。

三、請假微服務採用的DDD設計思想

請假微服務中用到了很多DDD設計思想和方法，主要包括以下幾點。

1.聚合的管理：聚合根、實體和值對象的關係。

2.聚合數據的初始化和持久化：工廠和倉儲模式。

3.聚合的解耦：聚合代碼的解耦、跨聚合的服務調用和對象解耦。

4.領域事件管理：領域事件實體結構、持久化和事件發佈。

5.DDD分層架構：基礎層、領域層、應用層和用戶接口層的協作。

6.服務的分層與協作：實體方法、領域服務、應用服務、接口服務，服務的組合和編排，跨多個聚合的服務管理和協同。

7.對象的分層和轉換：DTO、DO和PO等對象在不同層的轉換和實現過程。

8.微服務之間的訪問：登錄和認證服務。
