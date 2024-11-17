---
Tags: 
  - C語言
  - 新手
Categories:
  - 語言
TocOpen: true
keyword:
    - C語言
    - 新手
    - 工程師
author:
    - Ender
description:
    - 從頭開始學習C語言-基本概述
comments: true
cover:
  alt: ''
  caption: ''
  image: ''
  relative: false
date: '2024-11-17'
description: '哈囉大家好，先自我介紹一下，我是轉職班出來的後端工程師，目前工作使用Laravel框架去開發，搭建此部落格是為了記錄自己學習，也希望分享給其他人，如果有誤歡迎跟我說。' # 開頭簡介
disableShare: true
draft: false # 是否發佈 true
hidemeta: false
lastmod: '2024-11-17'
showToc: true
showbreadcrumbs: true
slug: 'C-learning-day-3'
title: 從頭開始學習C語言-基本概述
weight: null # 置頂
---

## C語言基本的概述

接下來我們來看一隻基本的C語言程式
我們在昨天建立的資料夾中新增test2.c檔案
並且寫下
```=c
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    int num;
    num = 2;
    printf("I have %d cats.\n", num);
    printf("You have %d cats, too.\n", num);
    system("read -p 'Press Enter to continue...'");
    return 0;
}
```

接著存檔、編譯執行看看。
應該可以看到下面有兩行輸出
```
I have 2 cats.
You have 2 cats, too.
```
別急，我們來一一解釋
### 第一行 `#include <stdio.h>`
這行代表的是告訴電腦將stdio.h這個檔案包含進去，這個檔案是 `standard input/output` 的縮寫，也就是標準輸入與輸出，只要是C語言有關輸入與輸出函數的格式，都是定義在這個檔案之中，因為我們的程式中有使用到printf()，而printf()是定義在stdio.h，所以我們需要將stdio.h包含進來。

### 第二行 `#include <stdlib.h>`

這行與第一行相同，只是system()函數是定義在stdlib.h中，所以我們要將他包括進去。**特別注意: 昨天我們在`test.c`中有使用到`system(pause)` 今天我們寫的是`system("read -p 'Press Enter to continue...'")` 這兩行功能相同，都是將執行畫面暫停，讓我們可以看到程式執行的情況。只是作業系統使用的指令不同**

### 第三行 `int main(void)`

我們在這定義了main()函數，定義的範圍從第四行的`{` 到第十一行的 `}`為止。習慣上我們將main()稱為主函數，因為是程式開始的起點，並且每一個獨立的C程式都必須要有main()才能執行。

而int 是表示main()有一個傳回值，傳回的型態是整數(integer)。main()括號中的void則是代表main()不需要任何的引數。

void有空無一物之意。

### 第五行 `int num`

宣告num是一個整數型態的變數，C語言需要在使用變數之前先宣告其型態。

### 第六行 `num = 2`

把整數2設定給整數變數num存放。

### 第七行 `printf("I have %d cats.\n", num)`

printf()是一個函數，先將`%d`以num值取代，接著將雙引號之間的文字輸出在螢幕上。
所以就會變成 `I have 2 cats.\n`
\n 是換行符號

### 第八行 `printf("You have %d cats, too.\n", num)`

與第七行相同。

### 第九行 `system("read -p 'Press Enter to continue...'")`

程式執行完畢後會自己關閉視窗，所以我們必須讓系統下這行指令，使程式暫停。

### 第十行 `return 0`

可由main()函數回傳整數0，數值由系統接收，習慣上回傳0代表程式執行成功。若有其他整數，可能程式出了狀況。

也因為我們要回傳整數0，所以我們在前面有定義 main() 是int。


## 詳讀

### include

接著我們來看看剛剛寫的include。
`stdio.h`，`stdlib.h`這種檔案我們稱為標頭檔(header file)，之所以稱為標頭檔，是因為他們被包括在程式碼的起頭。
當程式加入

`#include <標頭檔>`

在程式編譯的時候就會將檔案的內容取代 `#include <標頭檔>`

那有人會問，使用標頭檔會使程式肥大嗎？
答案是不會，編譯器只會去依照撰寫內容去截取需要的資訊。

### 主函數main()

C程式是由相當多函數所組合，包括main()與printf()都是C語言所提供標準函數，main()是不可缺的函數，是程式執行的開端。

### 變數

想要宣告一個可以存放整數的變數，變數名稱為num

`int num`

也可以多個宣告

`int num1, num2, num3`

### 變數資料型態

有字元(char), 整數(int), 長整數(lang), 短整數(short), 浮點數(float), 倍精度浮點數(double)等型態，也可以決定變數為有號(sign), 無號(unsigned), 有號可以存放正數或負數，無號只能存放正數。


### 變數設值

我們可以在宣告的同時設定值

`int num = 2;`

也可以先宣告再設定

`int num;`
`num = 2;`


## 結語

今天我們從一個基本的C程式去看看到底是怎麼執行的，也看到基本的C程式構成，下次我們就來介紹基本的資料型態！其實書中還有提到許多，但我只節錄一些我自己想要記下的，所以如果想知道更詳細的資料或想更深入學習，還是建議去買本書喔！

## 參考書籍

C語言教學手冊-洪維恩