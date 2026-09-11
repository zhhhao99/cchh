# FlowUs 风格固定媒体页面

此版本重点是“固定图片/视频位置”：

- 图片 1 永远位于第一部分正文后；
- 视频 1 永远位于第二部分正文后；
- 图片 2 永远位于补充说明后；
- 上传/替换媒体不会新增卡片，也不会改变顺序；
- 页面主体采用接近 FlowUs 的文档式排版。

## Gitee Pages 发布

把整个目录上传到仓库根目录：

index.html
assets/image-1.svg
assets/image-2.svg
assets/video-poster.svg

然后开启静态网站托管即可。

## 两种替换媒体方式

### A. 正式发布（推荐）
直接把实际图片替换为固定文件，例如：
assets/image-1.jpg
assets/image-2.jpg

并把 index.html 对应的 src 改成这些路径。

视频也可以直接放：
assets/video-1.mp4

然后给 `<video id="video1">` 增加 `src="assets/video-1.mp4"`。

这种方式所有访客都能看到同样的内容。

### B. 网页内“编辑页面”
点击右上角“编辑页面”后，可在固定位置选择本机图片/视频。
这些文件只保存到当前浏览器 IndexedDB，不会上传到 Gitee，其他访客看不到。

## 关于原 FlowUs 链接

当前抓取环境访问该分享链接超时，因此无法可靠读取原页面块内容和精确顺序。
本版本采用接近 FlowUs 的视觉样式和固定媒体插槽设计，而不是声称对原页面做了像素级复制。
如提供整页截图、PDF 或 Markdown 导出，可以继续把正文和每个图片/视频插槽精确对齐。
