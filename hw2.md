## 專案管理

### 甘特圖

```mermaid
gantt
    title A Gantt Diagram

    section 任務
    研擬計畫           :a1, 2014-01-01, 1d
    任務分配           :a2, after a1, 4d
    取得硬體           :a3, after a1, 17d
    程式開發           :a4, after a2, 70d
    安裝硬體           :a5, after a3, 10d
    程式測試           :a6,after a4, 30d
    撰寫使用手冊       :a7, after a5, 25d
    轉換檔案           :a8, after a5, 20d
    系統測試           :a9,after a6, 25d
    使用者訓練          :a10, after a7, 20d
    使用者測試          :a11, after a9, 25d
```

### PERT/CPM圖

```graphviz
digraph {
	node[shape=record];
	rankdir="LR";
    no1 [label = "研擬計畫 | 任務1 | 開始:第1天 | 結束:第2天 | 需時:1天"]
    {rank=same;no2 no3}
    no2 [label = "任務分配 | 任務2 | 開始:第2天 | 結束:第6天 | 需時:4天"]
    
    no3 [label = "取得硬體 | 任務3 | 開始:第2天 | 結束:第19天 | 需時:17天"]
    no1->no2
    no1->no3
    no4 [label = "程式開發 | 任務4 | 開始:第6天 | 結束:第76天 | 需時:70天"]
    
    no2->no4
    
    no5 [label = "宣告訓練 | 任務5 | 開始:第19天 | 結束:第29天 | 需時:10天"]
    no6 [label = "程式測試 | 任務6 | 開始:第76天 | 結束:第106天 | 需時:30天"]
    no3->no5
    no4->no6
    no7 [label = "撰寫使用手冊 | 任務7 | 開始:第29天 | 結束:第54天 | 需時:25天"]
    {rank=same;no7 no8 }
    no8 [label = "轉換檔案| 任務8 | 開始:第29天 | 結束:第49天 | 需時:20天"]
    no5->no7
    no5->no8
    no9 [label = "系統測試| 任務9 | 開始:第106天 | 結束:第131天 | 需時:25天"]
    no6->no9
    no10 [label = "使用者訓練| 任務10 | 開始:第54天 | 結束:第74天 | 需時:20天"]
    no7->no10
    no8->no10
    no11 [label = "使用者測試| 任務11 | 開始:第131天 | 結束:第156天 | 需時:25天"]
    no9->no11
    no10->no11
}
```


### 關鍵路徑
