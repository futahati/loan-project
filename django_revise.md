- Django課程

# 下載、安裝程式
## git(2026/4/13)
- 網站 https://git-scm.com/
- 下載
	- 點擊 Install for Windows
	- 轉新視窗後，點擊 Git for Windows/x64 Setup. (2026/4/13)
- 安裝
	- 雙擊 Git-2.53.0.2-64-bit (2026/4/13)

## vscode(2026/4/13)
- 網站 https://code.visualstudio.com/
- 下載
	- 點擊 Download for Windows
	- 轉新視窗後，再自動跳出下載視窗，按「存檔(S)」
- 安裝
	- 雙擊 VSCodeUserSetup-x64-1.115.0 (2026/4/13)
	- 一堆英文(詢問不使用系統管理員安裝)，按「確定」
		This User Installer is not meant to be run as an Administrator. If you would like to install VS Code for all users in this system, download the System Installer instead from https://code.visualstudio.com. Are you sure you want to continue?
	- 授權合約 => 打勾勾 □我同意
	- 選擇附加的工作 → 附加圖示： => 打勾勾 □建立桌面圖示(D)
		- 其他不做任何修改
	- 安裝完成 => 取消勾勾 □啟動 Visual Studio Code

## python(2026/4/13)
- 網站 https://www.python.org/
- 下載
	- 點擊 Downloads
	- 點擊 Or get the standalone installer for 後的 按鈕Python 3.14.4 (2026/4/13)
- 安裝
	- 雙擊 python-3.14.4-amd64 (2026/4/13)
	- 打勾勾 => □ Add Python to PATH

## MySQL
- https://www.mysql.com/


# 設定
## git
- 
## vscode
- File => Preferences => Settings
	- 搜尋欄位輸入
		1. Color
			- Workbench: Color Theme
				- 打勾勾
				- 用途：調整編輯器的背景色，以及不同類型的程式碼（變數、關鍵字、註解）要顯示成什麼顏色
		1. Mouse
			- Editor: Mouse Wheel Zoom
				- 打勾勾
				- 用途：滑鼠滾輪縮放，快速調整字體大小
		1. Format
			- Editor: Format On Save
				- 打勾勾
				- 用途：存檔時自動格式化，讓程式碼永遠整齊
			- Editor: Default Formatter
				- 下拉選單 => HTML Language Features
				- 用途：預設格式化器，指定誰來幫你排版
				- **重要性： 如果你發現 `Format On Save` 沒反應，通常是因為你還沒設定這項**
			- Editor: Format On Paste
				- 打勾勾
				- 用途：在貼上時自動格式化（自動縮排、清理間距、對齊符號）
		1. Exclude
			- Files: Exclude(排除清單)
				- 將清單裡的 **/.git 刪除，形成可見的資料夾。
				- **功能：設定哪些檔案或資料夾「不應該」出現在左側的檔案瀏覽器中，或是「不應該」被搜尋功能搜到**
- Ctrl + Shift + X 「Extensions」（擴充功能）面板
- Install時出現新視窗，安裝 VS Code 擴充功能（如 Python）時，因為安全機制（Workspace Trust）攔截而跳出的最後確認視窗。
	- Do you trust the authors of the files in this workspace?Enabling this extension requires a trusted workspace.If you don't trust the authors of these files, we do not recommend continuing as the files may be malicious. See our docs to learn more.
	- 點擊 Trust Workspace & Install (信任工作區並安裝)
- 搜尋欄位輸入
	- python
		- 用途：會自動去連結電腦裡已經裝好的 Python 引擎，提供你語法突顯、自動格式化（就是你前面問的 Format on Save）等功能
	- Black Formatter
		- 用途：當一個全自動的程式碼管家，只要一按下 Ctrl + S 存檔，Black 會在 0.1 秒內把程式碼排版得漂漂亮亮。
	- Dracula Theme Official
		- 用途：「換膚」，讓你的 VS Code 介面變得超級酷炫且護眼
		- 上方搜尋欄出現（3擇1）
			- Dracula Theme (經典版)
			- Dracula Theme Soft (柔和版)
			- Dark High Contrast (深色高對比)
		- 手動啟用方式：
			1. 按下快捷鍵 Ctrl + K，接著按 Ctrl + T (或是點擊左下角的小齒輪 -> Themes -> Color Theme)
			1. 在彈出的清單中選擇 「Dracula」
	- Live Server(在初期練習寫靜態網頁（前端介面）時，非常好用)
		- 用途：在網頁開發時，只要一按存檔（Ctrl + S），瀏覽器就會自動重新整理，網頁即時看到修改後的樣子
		- **多裝置同步測試**
			- **只要你的手機和電腦連在同一個 Wi-Fi，你可以在手機上輸入電腦的 IP，這樣你在電腦改程式碼，手機上的網頁也會跟著同步更新，非常方便測試手機版網頁**
		- VS Code 的介面
			- 右下角狀態列： 會出現一個 「Go Live」 的小圖示。
			- 啟動方法： 打開你的 index.html 檔案，點擊右下角的 Go Live，它就會自動幫你開啟瀏覽器。
			- 停止方法： 點擊右下角的 Port: 5500，就能關閉伺服器。

	- 其他換膚
		- One Dark Pro (最受歡迎的 Atom 風格)
		- GitHub Theme (官方原味)
		- Night Owl (專為深夜工作設計)
		- Gruvbox Theme (復古懷舊風)
		- Tokyo Night (霓虹東京)


## python


# 專案開發(Vscode)
- File => Open Folder
	- Do you trust the authors of the files in this folder?Code provides features that may automatically execute files in this folder.If you don't trust the authors of these files, we recommend to continue in restricted mode as the files may be malicious. See our docs to learn more.C:\Users\USER\Desktop\Django
	- 打勾勾 □ Trust the authors of all files in the parent folder 'Desktop'?
	- 點擊 Yes, I trust the authors

# 申請網站
## GitHub
- https://github.com/
## TiDB Cloud
- https://auth.tidbcloud.com/login?state=hKFo2SA1UkdLczBFWlhrZ2djc0ZBTEYxdXo0OFJSUEFWT20xM6FupWxvZ2luo3RpZNkgaDBaN2xpV0wycXNhV1pGWVE4dkZ6NlhjUjlGSmJXS0qjY2lk2SA2SVp0aENmbVJLSVBFblFTVDhhRGJ0TTdTR2RNbmlSbA&client=6IZthCfmRKIPEnQST8aDbtM7SGdMniRl&protocol=oauth2&response_type=token%20id_token&redirect_uri=https%3A%2F%2Ftidbcloud.com%2Fauth_redirect%3Fprev%3D%252F&scope=openid%20email&nonce=wC~x4ZCJDiyUgPKVCew.u__iphzBDVO0&auth0Client=eyJuYW1lIjoiYXV0aDAuanMiLCJ2ZXJzaW9uIjoiOS4xOS4xIn0%3D