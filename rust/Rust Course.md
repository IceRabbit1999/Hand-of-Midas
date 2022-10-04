[Rust 语言圣经 - Rust 语言圣经 (Rust Course)](https://course.rs/about-book.html)

[toc]

# 1. 快速开始

1. 什么情况下该把 `Cargo.lock` 上传到 git 仓库里？很简单，当你的项目是一个可运行的程序时，就上传 `Cargo.lock`，如果是一个依赖库项目，那么请把它添加到 `.gitignore` 中

# 2. Rust基础入门

## 2.1 变量绑定与解构

### 使用下划线开头忽略未使用的变量 

`let _unused = 5;`

### 变量解构

从一个相对复杂的变量中，匹配出该变量的一部分内容

应该是对应destructing