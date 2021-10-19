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

### git graph 查看視覺化資訊


## Part 3: GitHub

先創建GitHub帳號，新增一個專案資料夾(repository)

開好會看到這個畫面

![image](/github_new_repo.PNG)




### 設定遠端資料夾指令

檢視遠端資料夾(repo)
```
git remote -v
```

設定遠端資料夾
一開始會沒東西，把剛剛新建好的頁面其中一行指令貼下來進行設定
```
git remote add origin https://github.com/你的網址-請自行修改.git
```

設定成功的畫再輸入一次git remote -v就會看到遠端資料夾連結了


### 把本地端的資料推到GitHub上面

推上遠端的指令 (備註，main的地方打你本地端的分支名稱，可能是master 或其他分支名)
```
git push origin main
```

如果每次要推上GitHub不想要打那麼長，可以用以下指令設定，這樣以後只需要打git push就可以推上去了。

設定
```
git push -u origin main
```



