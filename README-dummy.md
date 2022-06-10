# Kindle_download_helper

Download all your kindle books script without programming knowledge and local dev setup.



## if you are like me as a programming  dummy with little techinical background and tired of python/docker etc.

### without any local installation or dev setup

follow these 4 steps 

**fork this repo**
**click action**
**grab csrf ** more see at how to grab cookie
**run workflow**


https://user-images.githubusercontent.com/2363295/173043109-a17ec588-f32a-4075-a2f3-c00bfa4235d3.mp4



### download an easy to use GUI 

<img width="1661" alt="image" src="https://user-images.githubusercontent.com/15976103/172113700-7be0ae1f-1aae-4b50-8377-13047c63411b.png">

下载二进制文件

到 [Release](https://github.com/yihong0618/Kindle_download_helper/releases) 页面查看最新版本，获取对应系统的二进制文件下载解压即可。

若打开二进制遇到问题，请参考[这个 issue](https://github.com/yihong0618/Kindle_download_helper/issues/25)






##  how to grab cookie

### if you are using `amazon.cn` 

1. 登陆 amazon.cn
2. 访问 https://www.amazon.cn/hz/mycd/myx#/home/content/booksAll/dateDsc/
3. 右键查看源码，搜索 `csrfToken` 复制后面的 value
4. 执行 `python3 kindle.py ${csrfToken} --cn`
5. 如果下载推送文件 `python3 kindle.py ${csrfToken} --cn --pdoc`

###  if you are using `amazon.com`

1. login amazon.com
2. visit https://www.amazon.com/hz/mycd/myx#/home/content/booksAll/dateDsc/
3. right click this page source then find `csrfToken` value copy
4. run: `python3 kindle.py ${csrfToken}`
5. if is doc file `python3 kindle.py ${csrfToken} --pdoc`

### amazon.jp` を使用する

1. amazon.co.jpにログインする。
2. ホームページ https://www.amazon.jp/hz/mycd/myx#/home/content/booksAll/dateDsc/）にアクセスする。
3. ソースコード上で右クリックし、`csrfToken`を検索して、それ以降の値をコピーします。
4. `python3 kindle.py ${csrfToken} --jp` を実行する。
5. プッシュファイルをダウンロードする場合 `python3 kindle.py ${csrfToken} --jp --pdoc`



## 注意

- cookie 和 csrf token 会过期，重新刷新下 amazon 的页面就行
- 程序会自动在命令执行的目录下创建 `DOWNLOADS` 目录，书会下载在 `DOWNLOADS` 里
- 如果你用 [DeDRM_tools](https://github.com/apprenticeharper/DeDRM_tools) 解密 key 存在 key.txt 里
- 或者直接拖进 Calibre 里 please google it.
- 如果过程中失败了可以使用 e.g. `--resume-from ${num}`
- 如果出现名字太长的报错可以增加: `--cut-length 80` 来截断文件名
- 支持推送文件下载 `--pdoc`

<img width="1045" alt="image" src="https://user-images.githubusercontent.com/15976103/172113475-92862b57-bb39-4cd7-84d5-6bc428172bc4.png">

## Enjoy

## 贡献

1. 任何 issues PR welcome
2. `black kindle.py`

## 赞赏

- 谢谢就够啦
- 分享给需要的人就更好了
