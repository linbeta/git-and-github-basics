# 基本指令

10/19助教課內容


## Part 1: 先安裝git、設定帳號，vs code可以安裝git graph

設定基本資料指令

1. 設定名字
```
git config --global user.name "你的名字"
```
設定email
```
git config --global user.email "你的email (MY_NAME@example.com)"
```

安裝git graph
![image](/安裝git_graph.PNG)


## Part 2: 基本Git使用指令


先隨意開一個新的資料夾來練習看看

在想設定git追蹤的資料夾開啟cmd視窗
![image](/open_cmd.PNG)


設定git開始追蹤此專案資料夾
```
git init 
```
再來專案資料夾就開始任意新增檔案、可以任意編輯寫些code或文字

stage指令：將所有未追蹤檔案移至staged區域
```
git add .
```

commit指令：將所有staged指令正式commit，並加上commit message
```
git commit -m "text"
```

查看git追蹤狀態的指令，這個使令隨時都可以使用
```
git status
```

查看commit的記錄檔
查看詳細記錄
```
git log
```
查看簡短版的紀錄檔
```
git log --oneline
```
