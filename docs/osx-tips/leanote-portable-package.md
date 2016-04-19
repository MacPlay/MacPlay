# leanote 开发版便携傻瓜包

前几天给手头的小白清洁安装了 Yosemite 10.10.2 版，格盘前备份资料时留了个心眼儿，给 leanote 开发版也顺手打了个压缩包。因为之前按照 [官方手册][leanote install manual] 安装 leanote 挺折腾的，这么短时间内所有流程再来一遍我得多蛋疼 (−_−＃) 所以先备份再说看看重装系统后能不能对压缩包进行二次利用。

重装完系统后再看了遍 [官方手册][leanote install manual]，仿佛恍然大悟一样：貌似直接解压打包好的文件，导入环境变量就能运行啊。啥折腾都不用了哇，啊哈哈～

动手试了下，果然没错！在此分享下具体步骤：

1. 下载 [压缩包][baidupan] 到当前用户根目录下，双击解压。(文件名：`home.zip`)

2. 导出 mongodb 环境变量并运行。复制以下内容粘贴到终端回车：

        export PATH=$PATH:~/home/user1/mongodb-osx-x86_64-2.6.7/bin
        mongod --dbpath ~/home/user1/data --auth

3. 新开终端标签页，导出 go 环境变量并运行 leanote 。

        export GOROOT=~/home/user1/go
        export GOPATH=~/home/user1/gopackage
        export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
        revel run github.com/leanote/leanote

以上命令都没有返回错误提示的话，现在你打开浏览器输入"http://localhost:9000"回车就可以访问搭建好的 leanote 网站啦～

如果你只想在本机运行 leanote，该压缩包应该是挺简单快捷的方法了。当然你也可以搞开发，只需把环境变量添加到bash_profile(或官方手册的/etc/profile)。好处是无需翻qiang龟速下载、没有安装权限提示、不必再次配置一遍，拿到任何新装机器上都可以用。非常绿色便携！而对于我来说，配合 LiveStyle 实时预览主题 CSS 样式很嗨皮啊～更新方面，鉴于 go 以及 mongodb 版本一般情况下不会有啥大的变化，而 leanote 依照 [官方手册][leanote install manual] 更新就可以了。

该压缩包目前只适用于 Mac OS X，但在其它系统环境下应该也可以这么搞：替换掉相应的 go/mongodb 文件夹就可以了嘛。

_打包好的文件包含了新建的账户和密码，但该密码早已弃用很久。所以也不是啥大问题，不删了就这样了～_

[baidupan]:http://pan.baidu.com/s/1eQD0TFk "http://pan.baidu.com/s/1eQD0TFk"

[leanote install manual]:https://github.com/leanote/leanote/wiki/leanote-develop-distribution-installation-tutorial "https://github.com/leanote/leanote/wiki/leanote-develop-distribution-installation-tutorial"
