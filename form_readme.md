# Form表單

- 參考網站 https://steam.oxxostudio.tw/category/html/tags/form.html

## 標籤語法

|                語法                | 說明                                                       |
| :--------------------------------: | :--------------------------------------------------------- |
|     \<form action=""> \</form>     | 「容器元素」；顯示類型為「block 塊級元素」，預設會強制換行 |
|     \<label for=""> \</label>      | 欄位標題元素                                               |
|        \<input type="text">        | 輸入(框)元素                                               |
| \<select name="" id=""> \</select> | 下拉選單元素                                               |
|   \<option value=""> \</option>    | 構成下拉選單的選項                                         |
|        \<button> \</button>        | 按鈕元素                                                   |

---

## \<form>容器元素

> \<form action="" method=""> \</form>

- action
  - 目標網址，要將資料發送到的位置
- method 屬性
  - 資料傳輸的 HTTP 協議，通常使用 get 或 post
- name 屬性
  - 表單名稱；若有多個表單元素時，每個表單的名稱**不可重複**
- target 屬性
  - 伺服器處理資料回傳後，顯示資料的位置
- autocomplete 屬性
  - 表單欄位是否會自動輸入 ( 有輸入過、瀏覽器該功能有開啟的狀態下 )，預設為 on 可設定 off
