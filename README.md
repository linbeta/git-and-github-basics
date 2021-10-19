# Git & GitHub 基本指令與操作

10/19助教課內容


## Part 1: 先安裝git、設定帳號，vs code可以安裝git graph

到Git的官網安裝：[https://git-scm.com/](https://git-scm.com/)

[中文版的Git入門](https://backlog.com/git-tutorial/tw/intro/intro2_1.html)



安裝完成以後輸入以下指令確認安裝版本
```
git --version
```

### 設定基本資料指令

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

點vs code左下角的Git Graph就可以查看了

![image](/gitgraph.PNG)


這是在vs code上看到的commit logs

![image](/commit_msg_on_vs_code.PNG)



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

推上遠端的指令 (備註，master的地方打你本地端的分支名稱，可能是main 或其他分支名)
```
git push origin mster
```

如果每次要推上GitHub不想要打那麼長，可以用以下指令設定，這樣以後只需要打git push就可以推上去了。

設定
```
git push -u origin master
```

#### 注意事項

GitHub上面預設的主分支名字是main，本地端是master，如果沒有改分支名，直接推上去，會在GitHub上再新增一個master分支，如果推上去有成功但沒看到資料，可以切換到master就看到程式檔了。

![image](/branch_name.PNG)


### 下載GitHub上面的資料

在GitHub上面的公開專案，右上角有個綠色的Code按鈕，點下去會看到Clone網址，如下圖：

![image](/git_clone.PNG)


輸入以下指令下載整個專案資料夾到本地
```
git clone https://github.com/linbeta/git-and-github-basics.git
```
