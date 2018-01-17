---

copyright:
  years: 2017
lastupdated: "2017-07-13"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# 管理備份
{: #backups}

您可以從服務儀表板的*備份* 頁面中建立及下載備份。提供有排程備份及手動備份。

## 檢視現有備份

資料庫的每日備份是自動排定的。若要檢視現有備份，請執行下列動作：

1. 導覽至服務儀表板。
2. 按一下標籤中的**備份**，以開啟_備份_ 頁面。即會顯示可用備份的清單：

  ![可用備份](./images/elastic_search-backups-show.png "可用備份的清單。")

按一下對應列來展開任何可用備份的選項。

![備份選項](./images/elastic_search-backups-options.png "備份的選項。") 

## 建立手動備份

除了排程備份外，您也可以手動建立備份。若要建立手動備份，請遵循步驟來檢視現有備份，然後在可用備份的清單上方按一下**立即備份**。即會顯示一則訊息，讓您知道已起始備份，且已將「擱置」備份新增至可用備份的清單。

## 備份內容

{{site.data.keyword.composeForElasticsearch}} 備份是使用 Elasticsearch API 中的 Snapshot 公用程式所取得的。此處理程序是以非封鎖方式在整個叢集上執行，因此所有編製索引及搜尋作業在其執行時，可以繼續正常執行。復原點備份是在建立 Snapshot 的時刻進行。

## 還原備份
若要將備份還原至新的服務實例，請遵循步驟來檢視現有備份，然後按一下對應列以展開您要下載之備份的選項。按一下**還原**按鈕。即會顯示一則訊息，讓您知道已起始還原。新的服務實例會自動命名為 "elasticsearch-restore-[timestamp]"，而且在佈建開始時，儀表板上會出現這個實例。