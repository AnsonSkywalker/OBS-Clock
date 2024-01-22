# OBS-Clock
一个在OBS内显示当前时间的应用。An application for displaying the current time within the OBS

使用教程：

1. 在场景内添加一个“浏览器”源
2. 勾选“本地文件”复选框，设置本地文件目标为该项目根目录下的`clock.html`文件
3. 根据你的需要自己调整浏览器源的宽度和高度（例如720p分辨率，即宽1280高720。可能需要配合“裁剪/填充”滤镜使用）
4. 将以下文本粘贴进自定义CSS样式内：

        body {
            background-color: #000;
        }
        #app{
            margin: 0px auto;
        }


        #app .clock {
            text-align: center;
            vertical-align: middle;
            display: inline-block;
            -webkit-text-size-adjust: 100%;
            -webkit-tap-highlight-color: transparent;
            line-height: 1.6;
            font-weight: 300;
            box-sizing: border-box;
            white-space: nowrap;
            font-family: clockicons, sans-serif;
            color: #EEE !important;
            font-size: 53px;
        }
    对于高级用户，可以根据你自己的需要自行修改CSS样式以自定义。
7. 根据你的需要自行调整“不可见时关闭源”和“场景变为活动状态时，刷新浏览器”设置项
8. 在场景中右键此浏览器源，调整“混合模式”为“添加”（透明背景，白色文字）或“减少”（透明背景，黑色文字）
