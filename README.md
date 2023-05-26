# vscode-wx-pinyin
微信小程序安装pinyin库，用于将中文字符串转化成拼音字母

## 1.安装node环境，官网下载安装版，和java jdk环境一样配就好了
![image](https://github.com/bobian29c6e/vscode-wx-pinyin/assets/70415754/b6a86f72-91dd-4596-b160-d7bcc86dcfc7)

## 2.能够使用npm命令后，终端进入项目文件，输入
```
npm init
```
项目文件就会生成一个 package.json 文件

## 3.继续再项目文件目录内，输入
```
npm i wl-pinyin
```

## 4.再微信开发工具内，点击工具->构建npm， 勾选“使用npm模块”

## 5.使用阶段：在js文件内头部添加
```
import pinyin from "wl-pinyin"
```
使用的时候可以
```
pinyin.getPinyin("你好") // 输出所有音频
pinyin.getFirstLetter("你好") // 输出首字母
//将拼音字母赋值给变量name
this.setData({
            name: pinyin.getPinyin(e.detail.value, '', false, false)
        })
```
