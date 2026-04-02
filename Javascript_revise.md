# JavaScript
- 在 HTML 裡，寫入位置在： \<body> 
    ```javascript
    <body>
        <!-- 畫面先出現（渲染） -->
            <h1>貸款精算小助手
                <span class="subtitle">輸入條件，快速分析您的還款計畫</span>
            </h1>

        <!-- 再使用下方的JavaScript控制 HTML程式碼 -->
            <!-- JavaScript 程式碼區 -->
            <script>

            const title = document.querySelector("h1");
            console.log(title); //後端顯示

            title.style.color = "orange";  //改變文字顏色
            title.innerText = "超級助手";  //改變文字
            title.innerHTML = "<b style='background-color: #3b98d2'>超級助手！</b>";  //可以針對html語法修改
            <\script>
    <\body>
    ```

## 基礎型態：字串 > 數字 > 布林值
- 在網頁取得的輸入都是「字串string型態」
- 每一段程式碼都要「；」分號結尾

### 數字 Number
- 整數、小數都是 Number
- consloe.log() ==> （函式）執行「把內容印出來」／網頁 console 輸出 == 後端顯示
    - console函式裡的 log方法
- typeof（運算子）==> 檢視型態
    ```js
    let a = 10;         // 整數
    let b = 20.7;       // 小數
    let f = a + b;      // 運算

    console.log(a, b, c);  //網頁console顯示 == 後端顯示
    console.log(typeof a, b, c, d, e, f);  //typeof 檢視變數的型態
    ```

### 字串 String
- 使用 `''單引號` or `""雙引號` or ``重音符（反引號） 包住
- 在 javascript 裡，數字可以加字串，結果是「以字串顯示」 => 代表`數字被字串同化`了！
- typeof（運算子）==> 檢視型態
    ```js
    let a = 10;         // 整數
    let b = 20.7;       // 小數
    let c = '51.36';    // 文字
    let d = "51.36";    // 文字
    let e = `你好！`;    // 文字
    let f = a + b + c + d + e;

    // 輸出結果是「字串String」，數字被字串同化
    console.log(f);  // 30.751.3651.36你好！
    console.log(typeof f);  // string

    // typeof 檢視變數的型態
    console.log(a, b, c, d, e);  // 10 20.7 '51.36' '51.36' '你好！'
    console.log(typeof a, typeof b, typeof c, typeof d, typeof e);  // number number string string string
    ```
- 樣板字串  (Template Literals) \` $ {} \`
    - 在${} 裡面放變數稱之為 「內插」 (Interpolation)
    - 重音符 (Backticks) \` \`
    - 錢字號與大括號 $ { }
    - 表達式 (Expression)：大括號裡面不只能放變數，還可以放簡單的數學運算
    ```js
    let a = 10;         // 整數
    let b = 20.7;       // 小數
    let c = '51.36';    // 文字
    let d = "51.36";    // 文字
    let e = `你好！`;    // 文字

    let f = a + b + c + d + e;
    console.log(a, b, c, d, e);  // 10 20.7 '51.36' '51.36' '你好！'

    // 樣板字串 \` $ {} \`
    console.log(`a = ${a} 型態：${typeof a}`);  // a = 10 型態：number
    console.log(`b = ${b} 型態：${typeof b}`);  // b = 20.7 型態：number
    console.log(`c = ${c} 型態：${typeof c}`);  // c = 51.36 型態：string
    console.log(`d = ${d} 型態：${typeof d}`);  // d = 51.36 型態：string
    console.log(`e = ${e} 型態：${typeof e}`);  // e = 你好！ 型態：string
    console.log(`f = ${f} 型態：${typeof f}`);  // f = 30.751.3651.36你好！ 型態：string

    // 放簡單的數學運算
    console.log(`f = ${a + b + c + d + e} 型態：${typeof (a + b + c + d + e)}`);  // f = 30.751.3651.36你好！ 型態：string
    ```
#### string常用方法
- str.lenght ==> 取得字串長度（字元數）
- str.toUpperCase() ==> 轉換全大寫
- str.toLowerCase() ==> 轉換全小寫
- str.includes("文字") ==>  判斷是否包含某段文字，回傳true/false
- str.indexOf(索引值) ==> 索引位置
- str.slice(開始索引值, 結尾索引值) ==> 擷取部份字串
- console.replace("原字串", "新字串") ==> 取代字串
- console.log(" 空白 ".trim()) ==> 去除頭尾空白，處理使用者輸入很實用


### 布林值 Boolean
- 只有 true, false
- 常搭配 if 判斷，控制程式哪條路。
    ```js
    let isStudent = true;
    let isLoggedIn = false;

    // 常用在判斷條件上
    if (isStudent){
        console.log("你是學生！");
    }
    ```

### 運算子 (Operator)
- 用來處理、計算或比較資料
- typeof ==> 對資料進行「型別檢查」的運算
- ３個＝ ==>(嚴格相等 / 全等) ； ２個＝ ==>(寬鬆相等)
- 加、減、乘、除、餘數、次方
    - 加法 `+` 碰到字串，就做串接，故 **加法要先轉型後，再相加**
        - 寫法： __Number("2")__
    - `減、乘、除` 無串接功能，會自動把字串轉成「數字」執行計算。
- 搭配 `const常數` 使用
    ```js
    let a = 10;
    let b = 20;
    
    console.log(a + b);    // + 看到字串，就做「串接」，結果就是字串
    console.log(a - b);
    console.log(a * b);
    console.log(a / b);
    console.log(a % b);    // 求餘數
    console.log(a ** b);   // 求次方
    ```
#### const 常數 ==> 宣告後不能再重新賦值 (不可變動／不可重新賦值)
- const 宣告變數後，此變數**不可變動**！！！
    - 變數名稱為：**英文大寫**
- 例：圓周率是固定數值，唯一的值。
    ```js
    <!-- 使用 let -->
    let pi = 3.14;

    pi = 3.18;  // 可修改pi值
    consloe.log(pi);
    ```
    ```js
    <!-- 使用 const常數 不可變動 -->
    <!-- const pi = 3.14; -->
    pi = 3.18;  // 不可修改pi值，在網頁 console 會報錯
    consloe.log(pi);

    const PI = 3.14;  // 變數名稱為「英文大寫」
    consloe.log(PI);
    ```
- 舉例：計算
    ```js
    const PI = 3.14;   // 常數；圓周率
    let r = 10;        // let非常數；半徑
    let area = r ** 2 * PI;  // 計算；圓面積

    console.log(PI, r, area);

    <!-- js很貴，什麼都要給 $ + {}大括號；使用 重音符`` 包住
    console.log(`圓周率：${} 半徑：${} 圓面積：${}`); -->

    console.log(`半徑：${r}公分 圓面積：${area}平方公分`);

    // 在 ${} 裡面直接寫計算公式也是可以的！
    console.log(`圓周率：${PI} 半徑：${r} 圓面積：${PI * r * r}`);
    ```
### prompt() 取得外部輸入 ==> HTML網頁跳出輸入框
```js
const PI = 3.14;   // 常數；圓周率
let r = prompt("請輸入半徑（cm）：");
let area = r ** 2 * PI;  // 圓面積

console.log(`半徑：${r}公分 圓面積：${area}平方公分`);
```

### .toFixed() ==> 執行完後，回傳的結果是「字串 (String)」，而不是數字！！
- 屬於 Number（數字物件） 的方法，會把數字轉成「指定小數點位數」的字串。
    ```js
    let height = prompt("請輸入身高（cm）：");
    let weight = prompt("請輸入體重（kg）：");
    let bmi = weight / (height / 100) ** 2;
    let Bmi = bmi.toFixed(2);

    console.log(`身高：${height} 體重：${weight} BMI：${bmi.toFixed(2)}`);  // 這是字串
    console.log(typeof Bmi);  // 輸出 "string"
    ```

## 陣列
- 用 [ ]中括號 建立
    - let fruits = [];
- .push() 新增元素（往陣列最後面加東西）
- .pop() 移除最後一個（取出，並刪除最後元素）
- .length 物件長度（回傳陣列有幾個元素）
- 舉例：計算bmi
    ```js
    let i = 0;

    let bmiRecord = [];  // 建立陣立，放輸入的值
 
    while (true) {
        let height = prompt(`第 ${i + 1} 次輸入=> 請輸入身高（cm）(q:離開)：`);

        // 離開的條件
        if (height === "q") break;
        // if (height.toLowerCase() === "q") break;  // 強制轉換為小寫

        let weight = prompt("請輸入體重（kg）：");

        let bmi = weight / (height / 100) ** 2;

        console.log(`身高：${height} 體重：${weight} BMI：${bmi}`);
        alert(`身高：${height} 體重：${weight} BMI：${bmi}`);
        i++;

        // 儲存 計算bmi的值，強制轉為「數值」
        bmiRecord.push(Number(bmi));

        }  //while迴圈結束

        let total = 0;

        // 取出每一次的BMI值
        for (let i=0; i<bmiRecord.length; i++) {
            console.log(`第 ${i + 1} 次輸入=> BMI：${bmiRecord[i]}`);   
            total =+ bmiRecord[i];
        }
        
        // 輸出平均BMI
        console.log(`平均BMI為： ${ (total / bmiRecord.lenght).toFixed(2)}`);
    ```
#### 用for迴圈 run 陣列


## 陳述句 (Statement)
### if (...) { }
- 程式的邏輯結構（如判斷、迴圈）
- prompt() ==> （函式）彈出輸入框
- isNaN() ==> （函式）檢查內容是不是「非數字」（Is Not a Number）
- alert() ==> （函式）彈出警告視窗
    ```js
    const PI = 3.14;   // 常數；圓周率
    let r = prompt("請輸入半徑（cm）：");
    let area = r ** 2 * PI;  // 圓面積

    if (isNaN(area)){
        console.log("輸入不正確唷～");   // 後端顯示
        alert("輸入不正確唷～");         // 前端視窗顯示
    }  // if判斷結束處

    console.log(`半徑：${r}公分 圓面積：${area}平方公分`);
    alert(`半徑：${r}公分 圓面積：${area}平方公分`);
    ```

### for (...) { }
- for ( 初始值; 條件式; 步進器 ) ==> 使用；分號！！
    - 初始值 `let i = 0`
    - 條件式 `i < numbers.length` ：.length 是「屬性」，物件的長度
    - 步進器 `i++` ：i++ 是「運算子」 (遞增運算)／ 若需要，亦可寫 i+=2（步進2）, i+=3（步進3）
```js
for (let i = 0; i < 5; i++ ) {
    let height = prompt("請輸入身高（cm）：");
    let weight = prompt("請輸入體重（kg）：");

    // 先使用
    // 呼叫函式；預設值point = 2 可寫、可不寫
    let bmi = getBmi(height, weight);  // 預設值point = 2 可寫、可不寫
    // let bmi = getBmi(height, weight, 4);  // 預設值point = 2 可寫、可不寫

    console.log(`身高：${height} 體重：${weight} BMI：${bmi}`);
    alert(`身高：${height} 體重：${weight} BMI：${bmi}`);
    }  //for迴圈結束
```
### while (true) {}
- break 離開迴圈
- continue 跳過某一次
```js
// 宣告i
let i = 0;

while (true) {
    let height = prompt(`第 ${i + 1} 次輸入=> 請輸入身高（cm）(q:離開)：`);

    // 離開的條件
    if (height === "q") break;
    // if (height.toLowerCase() === "q") break;  // 強制轉換為小寫

    let weight = prompt("請輸入體重（kg）：");

    // 先使用
    // 呼叫函式；預設值point = 2 可寫、可不寫
    let bmi = getBmi(height, weight);  // 預設值point = 2 可寫、可不寫

    console.log(`身高：${height} 體重：${weight} BMI：${bmi}`);
    alert(`身高：${height} 體重：${weight} BMI：${bmi}`);
    i++;  // i值累加

    }  //while迴圈結束
```

## function 函式 ==> 關鍵字宣告
- 先使用，再宣告。
- 駝峰式命名 `sayHello()`
- 可使用 `return`
- 宣告函式
    ```js
    function sayHello(){
        console.log("您好，世界！");
    }
    ```
- 呼叫函式
    ```js
    sayHello();
    sayHello();
    ```
### 舉例：計算BMI
```js
let height = prompt("請輸入身高（cm）：");
let weight = prompt("請輸入體重（kg）：");

// 先使用
// 呼叫函式；預設值point = 2 可寫、可不寫
let bmi = getBmi(height, weight);  // 預設值point = 2 可寫、可不寫
// let bmi = getBmi(height, weight, 4);  // 預設值point = 2 可寫、可不寫

console.log(`身高：${height} 體重：${weight} BMI：${bmi}`);
alert(`身高：${height} 體重：${weight} BMI：${bmi}`);

// 再宣告
// 宣告函式
function getBmi(height, weight, point = 2){
    let bmi = weight / (height / 100) ** 2;

    if (isNaN(bmi)) return "輸入錯誤！";

    // .toFixed() 會把 bmi數字 轉成 指定小數點位數 的 字串string
    return bmi.toFixed(point);
} // getBmi函式結束
```

## 函式／方法
- consloe.log() ==> （函式）執行「把內容印出來」
- prompt() ==> （函式）彈出輸入框
- isNaN() ==> （函式）檢查內容是不是「非數字」（Is Not a Number）
- alert() ==> （函式）彈出警告視窗

## 說明
- 每一段程式碼都要「；」號結尾
- let 變數 ==> 宣告後可以隨時修改內容(值可變動／可重新賦值)
- console.log() ==> 只有 console 輸出 == 後端顯示
    - console函式裡的 log方法
- typeof 檢視型態
    ```js
    let a = 10;         // 整數
    let b = 20.7;       // 小數
    let c = '51.36';    // 文字
    let d = "51.36";    // 文字
    let e = true;       // 布林值
    let f = a + b;

    console.log(a, b, c);  //網頁console顯示 == 後端顯示
    console.log(typeof a, b, c, d, e, f);  //typeof 檢視變數的型態
    ```
