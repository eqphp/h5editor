欢迎使用 H5Editor
===========================
H5Editor是一款所见即所得的JavaScript富文本编辑器；全面支持html5语义规范，自动适配PC、手机等移动设备的响应式网页布局；具备开源、好用、界面美观等极致化设计特点。

![](https://editor.yituodan.net/s/image/shortcut.png)

#### 这些功能是你正在寻找的吗？ #####
1.  仅允许 img、video、audio、a、b、i、em、span、cite、strong、p、pre、br、hr、blockquote、ul、ol、li、h1、h2、h3、h4、h5、h6、table、tbody、tr、th、td Html5常用标签和 class、src标签属性，有效杜绝XSS攻击；
2.  支持 emoji互动、图片上传、音视频播放、文件下载、地图位置等媒体资源，使用表格、列表、标题正文、引用、代码、分割线等分层次表现结构，使得网页内容丰富多彩，简洁明朗；
3.  支持从剪贴板粘贴图片，自动过滤从word、pdf、网页等复制内容所带样式，重新使用编辑器规范生成样式；
4.  支持PC、手机等响应式设计，自动适配各厂家设备屏幕尺寸，合理组局，界面美观，内容层次分明雅致；
5.  可视化编辑，所见即所得，配合源码编辑模式，可供高级开发人员快速调优；
6.  可自定义数据模型组件，支持特殊业务需求；
7.  兼容几乎市面上所有浏览器，随意选择，无后顾之忧。

#### 项目中接入方法 #####

STEP 1、从码云（或github）上下载H5Editor安装包，复制到到项目静态目录，并配置config.js文件中上传地址，媒体资源存放路径。
```javascript
const AE_path = {
    upload: '/upload/h5',
    emoji: '/emoji/',
    photo: '/file/static/picture/',
    video: '/file/static/video/',
    archive: '/file/static/archive/',
};
```
STEP 2、在需要使用编辑器的页面脚本末尾引入类库脚本。
```html
<script src="jquery.js"></script>
<script src="dialog-plus.js"></script>
<script src="paste.js"></script>
<script src="config.js"></script>
<script src="script.js"></script>
```
STEP 3、在内容编辑位置复制粘贴编辑器操作按钮、输入框。
```html
<div id="AE_editor">... </div>
<div contenteditable="true" class="AE_article">
<textarea id="AE_article" class="hide"></textarea>
```
STEP 4、提交表单时接收编辑器编辑内容。
```javascript
let content=$('.AE_article').html().replace(/\sid="_[_.]?\d{13}"/g,'');
```
STEP 5、在内容显示页面头部引入富文本样式表（也可以使用自己定义的）style.css。
```html
<link rel="stylesheet" href="style.css"/>
```

#### 快速编辑视频教程 #####
[![h5editor usage](https://editor.yituodan.net/s/image/video_face.png)](https://editor.yituodan.net/s/image/help_video.mp4)


#### 依赖第三方类库： #####

1.  1.7版本以上Jquery：[https://jquery.com/download/](https://jquery.com/download/)
2.  ArtDialog-plus：[http://aui.github.io/artDialog/](http://aui.github.io/artDialog/)
3.  剪贴板文本、图片粘贴paste：[https://github.com/layerssss/paste.js/](https://github.com/layerssss/paste.js/)


#### H5Editor更新订阅号：h5editor #####
![](https://editor.yituodan.net/s/image/subscribe.png)

#### 支持开源，多多建议 #####
我们承诺：您的任何留言建议我们会第一时间处理，若有不妥请务必QQ：2581221391（或邮件：eqphp_framework@126.com）联系。
