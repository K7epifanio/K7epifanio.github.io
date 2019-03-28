# Version control system
## Build local repo
### 基础知识
软件开发系统的版本控制系统分为一般在軟體開發中又分為中央式系統（例如：Subversion、CVS 等）與分散式系統（例如：Git、BitKeeper、mercurial 等），中央式版本控制系統的工作主要在一個伺服器進行，由中央管理存取權限「鎖上」檔案庫中的檔案，一次只能讓一個開發者進行工作。而分散式系統讓不同開發者直接在各自的本地檔案庫工作，並容許多個開發者同時更動同一個檔案，而每個檔案庫有另外一個合併各個改變的功能。分散式系統讓開發者能在沒有網路的情況下也能繼續工作，也讓開發者有充分的版本控制能力，而不需經中央管理者的許可，但分散式系統仍然可以有檔案上鎖功能。

### git and github

Git 是一個分散式版本控制軟體，最初由 Linus Torvalds 創作（也是作業系統 Linux 系統的開發者），其最初目的是為更好地管理 Linux kernel 開發而設計，其具備優秀的 merge tracing 合併程式碼的能力（使用程式碼 snapshot 來比較歷史版本差異）。

Github 則是一個支援 git 程式碼存取和遠端托管的平台服務，有許多的開放原始碼的專案都是使用 Github 進行程式碼的管理。若是讀者未來有志於從事程式設計相關工作的話，建議可以熟悉掌握 Git 和 Github 的使用，並建立自己的 Github profile 作品集。

![alt text](https://github.com/K7epifanio/K7epifanio.github.io/blob/master/git-workflow.png)





* // 建立一個 hello-git 資料夾
$ mkdir hello-git
* // 移動到 hello-git 資料夾
$ cd hello-git
* // 將專案資料夾建立成 git repository
$ git init
* // 列出專案資料夾下的檔案和資料夾（-l 參數為列出詳細資料，-a 為列出隱藏資料夾）
$ ls -la

与remote端的repo建立联系
* $ git config --global user.name "<Your Name>"
* $ git config --global user.email "<your@gmail.com>"

* git status查看当前仓库状态
* git add filename 添加文件到staging are
* git commit -m "Init filename" 提交到本地库

// 檔案尚未加入過追蹤時使用，即可恢復到檔案尚未加入暫存區
$ git rm --cached hello.py

// 若檔案已經在 repository 內，則使用以下指令
// repository 與 stage 的檔案都會被還原到 HEAD，但 working directory 內的檔案不變
$ git reset HARD

若有檔案修改，記得要再 add 修改的檔案（這是新手比較容易忘記的部分），若是要放棄修改可以使用 git checkout -- 檔案名稱


$ git push -u origin master push到云端
























## Reference
[Git 與 Github 版本控制基本指令與操作入門教學 \| TechBridge 技術共筆部落格](https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/)

[提交檔案【教學1 開始使用Git】 \| 連猴子都能懂的Git入門指南 | 貝格樂（Backlog）](https://backlog.com/git-tutorial/tw/intro/intro2_4.html)
