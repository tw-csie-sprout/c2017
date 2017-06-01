# 環境安裝

本次作業使用 Qt 的圖形使用者界面套件，為了避免環境問題，需要連 Qt 原生的整開發環境 Qt Creator 一起安裝。

## 下載 Qt5

[Donwload Link](https://www.qt.io/download-open-source/#section-2)

下載 Online Installer 

Windows 請選 For Windows，Mac 請選 for macOS

下載完畢後，開啟安裝程式

## 安裝 Qt5 、 Qt Creator、MinGW
1. 安裝程式歡迎畫面：直接點 `Next >` 下一步
2. 註冊與登入頁面：點 `Skip >` 下一步跳過即可
3. Qt 歡迎畫面：直接下一步
4. 取得資訊：它開始向遠端的伺服器取得資訊，這裡需要等幾十秒
5. 安裝路徑：安裝的地方保持預設的 `C:\Qt` ，下一步
6. 選擇安裝套件：我們要只需要基本功能就好，先點 `Deselect All` 取消選取全部 (Tools 沒辦法取消選取是正常的)，然後按一下 `Qt 5.8` 左側的 `+` 號展開細項，勾選 `MinGW 5.3.0 32bit`，下一步
7. 合約：選擇同意 `I have read and agree ...` ，下一步
8. 新增 Qt 至開始功能表：直接下一步 
9. 準備安裝：點 `Install` 開始安裝
10. 安裝：這裡它會下載資料並自動安裝在你的系統上，需要幾分鐘
11. 完成：點 `Finish` ，系統會自動開啟 Qt Creator

## 開啟專案

1. 點[這裡](https://drive.google.com/open?id=0B_Qu9g2Wq4PbUTdQTkpQcDBOY0k)，再點網頁右上角的箭頭，以下載這次作業用 ZIP 壓縮的「測試用」專案檔
2. 下載回來後，對檔案點右鍵並選擇「解壓縮全部」，指定路徑為**任一個全英文路徑的資料夾**，例如 `D:\sprout\ns-shaft-demo\` ，或者直接放桌面上。請務必確認資料夾路徑**沒有中文**，例如以下就是一個正確的例子
   ![](https://i.imgur.com/4XWPg3S.png)
3. 打開剛剛解壓縮在桌面的資料夾，開啟 `proj.pro` (Qt Project File) 專案檔
4. 它會跳出視窗問你要不要用該專案的環境設定，點 Yes，如果沒有跳視窗請直接去第 6 步
5. 點右邊的 Configure project
6. 點左下角的綠色三角形箭頭(編譯並執行)，試玩一下做一半的遊戲，如果可以執行代表你 Qt 環境安裝完成！
