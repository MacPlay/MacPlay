# asciinema - 更炫酷地记录和分享终端操作

具体请访问官网：[asciinema - Record and share your terminal sessions, the right way](https://asciinema.org)

基于文本的录屏工具，对终端输入输出进行捕捉，然后以文本的形式来记录和回放！这使其拥有非常炫酷的特性：在“播放”过程中你随时可以暂停，然后对“播放器”中的文本进行复制或者其它操作！实际效果可以点击下方的播放按钮查看。

具体原理简单点说，就是把终端显示和时间戳记录成 json 形式，然后使用 javascript 脚本解析出来。配合官方提供的 CSS 样式，乍看起来以为是视频播放器，然而它却是不折不扣的文本。相比视频录屏或 GIF 动图的方式，文件体积小的不可思议，不需缓冲即可播放，可以更方便的分享给他人或者嵌入到网页中。

安装和使用都非常简单：

终端中输入 `brew update && brew install asciinema` 即可安装。

使用方法：运行 `asciinema rec` 开始，录制完成后输入 `exit` 或按 `Ctrl-D` 结束。然后询问你是否上传，回车即可将录制文件上传到官网并得到访问链接。点击链接可观看刚记录的操作，并可选择分享该链接或进行其它操作。

对于将“录屏”操作嵌入到博客，官方提供了较详细的说明。然而从别的网站拉取所有文件，可能遭遇到功夫墙并且访问速度有些慢，于是看了下手册将其放到自家博客，试了下用户体验非常好。

以下嵌入的是为本博客添加 asciinema 支持的录屏步骤：

<div id="player-container"></div>
<script>
    asciinema.player.js.CreatePlayer('player-container', '/attachment/asciicast-49328.json', { width: 110, height: 29 });
</script>

<br>

小结：以后嵌入录屏文件，仅需粘贴以上代码行，修改 json 文件指向即可。json 文件可从本机临时文件夹（形似 `/var/folders/xv/r404ltkx1bbf52p2p6sql5b80000gn/T` ） 得到，或者录制时直接输入 `asciinema rec demo.json` 也可。
