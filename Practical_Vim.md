---
title: Vim 实用技巧
date: 2018-09-25
catalog: true
tags:
- Vim
---
## 模式
### 普通模式
### 操作符待决模式
### 插入模式
### 可视模式
#### 字符可视模式
v
#### 行可视模式
V
#### 列可视模式
`<C-v>`

#### 选择模式
用`<C-g>`切换选择模式和可视模式

### 命令模式 

## 移动
按键操作|效果
---|---
G|跳到最后一行
{n}G|跳到第n行
gg|跳到第一行
ctrl+f|向前翻一页
ctrl+b|向后翻一页

## 查找

### 行内查找

按键操作|效果
---|---
f{char}|正向查找
F{char} |反向查找
;|重复上次查找命令
,|反转方向重复上次查找命令


### 全文查找
按键操作|效果
---|---
/{string}|根据字符串检索
n|跳转到下一处匹配
N|跳转到上一处匹配
