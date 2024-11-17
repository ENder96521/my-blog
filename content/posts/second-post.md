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
    - 從頭開始學習C語言-安裝環境
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
slug: 'C-learning-day-2'
title: 從頭開始學習C語言-安裝環境
weight: null # 置頂
---

## 安裝開發環境

嗨，又過了一天，今天我們來學習如何去安裝自己的開發環境，由於我自己是用MacBook去開發，所以今天的範例就用MacOS做示範。而平常習慣用VSCode，所以我們也嘗試用VSCode看看

## 第一步 安裝Xcode

這步驟很簡單，就到App Store安裝即可。

## 第二步 安裝VSCode

這步驟也很簡單，去官網下載，相信大家也都會。

## 第三步 安裝延伸模組

到VSCode 延伸模組 分別安裝

* C/C++
* C/C++ Compile Run
* C/C++ Extension Pack

安裝完成後就可以開發C語言囉！
接下來我們來嘗試看看

## 開啟專案資料夾

接著我們在VSCode中建立資料夾
並且寫下基本的程式並命名為`test.c`

```=c
#include <stdio.h>
#include <stdlib.h>
int main() 
{
    printf("Hello C!\n");
    printf("Hello World!\n");
    
    system("pause");
    return 0;
}
```

## 執行

點選右上角的三角形按鈕，並選擇Run C/C++ File
接著選擇C/C++:clang++ build and debug active file
他就會幫你偵錯與編譯執行囉！

## 本日結語

今天相對是對於開發環境去做安裝，開發環境時通常伴隨著學習，有時候光是安裝環境就花了大半天了呢！所以不只這邊的資訊，大家也都可以去多多參考其他人所分享的文章喔！



