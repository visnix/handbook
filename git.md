## 生成密钥 
ssh-keygen -t rsa -C "youremail@example.com"

## 下载github中某个特定目录
https://github.com/WebKit/WebKit.git/trunk/Source/JavaScriptCore

svn export https://github.com/WebKit/WebKit.git/trunk/Source/JavaScriptCore

## 设置git proxy
在.gitcofig总写入
`
[https "https://github.com"]
	proxy = https://127.0.0.1:9090
`
