## TypeScript 11
## Chapter 11: TypeScript Project
It is my coding practice with the TUTORIAL of Dave Gray. 

## Source
### Dave Gray 的 TypeScript 資源
https://github.com/gitdagray/typescript-course

### Dave Gray 的 TypeScript 課程
https://youtube.com/playlist?list=PL0Zuz27SZ-6NS8GXt5nPrcYpust89zq_b&si=8IJALfXOcur2OO_K

### Dave Gray 的 YouTube 頻道
https://www.youtube.com/@DaveGrayTeachesCode

## Quick Concept offline
###  1. Intro
        教學影片開頭和介紹

###  2. Welcome

###  3. Project Intro
        設定一個列表，可以加入、移除、畫橫線和清除全部

###  4. Install Node.js
        Node.js 網站
        https://nodejs.org/zh-tw

###  5. Project Set Up with Vite
        (1)在 terminal 輸入 node -v 確認版本
        (2)在 terminal 輸入 npm create vite@latest
        (3)設定專案名稱為 TS11
        (4)選取框架 Vanilla，變體選擇 TypeScript
        (5)在 terminal 輸入 cd TS11，修改當前資料夾預設路徑
        (6)在 terminal 輸入 npm i，安裝
        (7)在 terminal 輸入 npm run dev，執行
        (8)開啟資料夾 TS11
        (9)刪除 counter.ts
        (10)新增資料夾 css, 移動 style.css
        (11)刪除 typescript.svg
        (12)刪除 vite.svg

###  6. Starter Code in Course Resources
        (1)修改 index.html, style.css
        (2)修改 style.css ，並匯入 main.ts 的路徑

###  7. Challenge 1: ListItem Class
        (1)新增資料夾 model
        (2)新增 ListItem.ts
        (3)匯出 Item 介面
        (4)匯出預設的 class 名稱為 ListItem，以 Item 介面為工具

###  8. Solution for Challenge 1
        (1)在 constructor 建構子，
        使用 private 關鍵字設定 id, item, checked 的類型和預設值
        (2)設定 id, item, checked 的 getter 和 setter

###  9. Challenge 2: FullList Class
        (1)新增 FullList.ts
        (2)匯入 ListItem
        (3)設定 List 介面
        (3A)設定 list 屬性的類型為帶有元素的 ListItem 陣列
        (3B)設定 load, save, clearList 方法的類型
        (3C)設定 addItem 方法的類型，
        參數為 itemObj，設定參數的類型
        (3D)設定 removeItem 方法的類型，
        參數為 id，設定參數的類型
        (4)匯出預設的 class 名稱為 FullList，以 List 介面為工具

### 10. Solution for Challenge 2
        (1)在 constructor 建構子，使用 private 關鍵字；
        使用 private 關鍵字設定 list 的類型和預設值
        (2)設定 static類成員
        instance 的類別為 FullList介面，作為修改過後的 FullList
        因為 load方法會回傳 FullList.instance
        (3)使用 getter 獲取 list，類型為帶有元素的 ListItem 陣列
        (4)設定 save 方法，儲存列表
        (5)設定 clearList 方法，清空列表
        (6)設定 addItem 方法，加入項目至列表
        (7)設定 removeItem 方法，移除項目至列表
        (8)設定 load 方法，載入列表
        (8A)宣告 storeList 從暫存儲存的列表，類型為 string 或 null
        (8B)宣告 parsedList 從暫存獲取的列表，
        參數 id 和 item 類型為 string，參數 checked 類型為 boolean，並以參數設定類型
        (8C)從暫存獲取的列表parsedList取得資料，將列表項目作為參數，
        宣告 newListItem，使用 addItem 方法更新列表

### 11. Challenge 3: ListTemplate Class
        (1)新增 ListTemplate.ts
        (2)匯入 FullList
        (3)設定 DOMList 介面，移除 index.html 的 unordered list
        (3A)設定 ul 的類型為 HTMLUListElement，即是 HTMLUnorderedListElement
        (3B)設定 clear 方法的類型
        (3C)設定 render 方法的類型，
        參數為 fullList，設定參數的類型

### 12. Solution for Challenge 3
        (1)匯出預設的 class 名稱為 ListTemplate，以 DOMList 介面為工具
        (2)在 constructor 建構子，使用 private 關鍵字；
        獲取 ul 元素 id 為 listItems，
        使用 as 指定類別為 HTMLUListElement，
        在 constructor 外層新增 ul 類型
        (3)設定 clear方法，清除的所有元素
        (4)設定 render方法，參數為 fullList，設定參數的類型
        (4A)新增 li, input, label, button 元素，宣告為 li, check, label, button
        (4B)新增 li 的 class
        (4C)新增 input(check) 的 type 和 id
        (4D)加入 check事件
        (4E)新增 label 的 for 和 文字內容
        (4F)新增 button 的 class 和 文字內容
        (4G)加入 button事件
        (4H)建構母元素和子元素的上下層關係
        
### 13. Pulling It Together in main.ts
        (1)匯入 style.css
        (2)匯入 FullList
        (3)匯入 ListItem
        (4)匯入 ListTemplate
        (5)宣告 initApp 和 文件載入事件
        (5A)宣告 fullList，singleton
        (5B)宣告 template
        (5C)宣告 itemEntryForm，設定類別
        (5D)加入 submit 事件於 itemEntryForm，避免列表重置
        (5E)宣告 clearItems，設定類別
        (5F)加入 click 事件於 clearItems，清理列表
        (5G)載入列表，渲染模板
        (5H)宣告 input
        (5I)宣告 newEntryText
        (5J)宣告 itemId
        (5K)宣告 newItem
        (5L)加入項目
        (5M)渲染列表

### 14. Does It Work?
        在 terminal 輸入 npm run dev，執行