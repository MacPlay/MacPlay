# asciinema - 更炫酷地记录和分享命令行操作

具体请访问官网：[asciinema - Record and share your terminal sessions, the right way](https://asciinema.org)

基于文本的终端命令行记录工具。简单来讲，就是把终端显示和时间戳记录成 json 形式，然后使用 javascript 脚本解析出来。配合官方提供的 CSS 样式，乍看起来就像是普通的视频播放器，然而它却是不折不扣的文本！相比传统的视频记录方式，文件体积小的不可思议，更加方便网络传播。同时及其重要的一点：因为是文本形式，在“播放”过程中你随时可以暂停，然后复制粘贴”播放器“中的命令文本！

终端中运行 `asciinema rec` 开始，录制完成后输入 `exit` 或按 `Ctrl-D` 结束。然后询问你是否上传，直接回车即可将录制文件上传到官网并得到访问链接。点击链接可观看刚记录的操作，或者分享该链接给其他人。

关于将“录屏”操作嵌入到博客，官方提供了较详细的说明。然而从别的网站拉取所有文件，可能遭遇到功夫墙并且访问速度有些慢，于是折腾了下将其放到自家博客，试了下用户体验非常好。

以下嵌入的是为本博客添加 asciinema 支持的操作：

<div id="player-container"></div>
<script>
    asciinema.player.js.CreatePlayer('player-container', '/attachment/asciicast-49328.json', { width: 110, height: 29 });
</script>

<br>

小结：以后嵌入录屏文件，仅需粘贴以上代码行，修改 json 文件指向即可。json 文件可从本机临时文件夹得到。
