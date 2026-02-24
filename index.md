<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>埃尔路德 - 剪辑作品集</title>
    <style>
        /* 全局基础样式 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: "PingFang SC", "Microsoft YaHei", sans-serif; 
            background-color: #f9f9f9; 
            color: #333; 
            line-height: 1.6;
        }
        
        /* 应聘必备：个人信息头部 */
        header { 
            background: #fff; 
            padding: 40px 20px; 
            text-align: center; 
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            margin-bottom: 30px;
        }
        header h1 { font-size: 2.5em; margin-bottom: 10px; color: #222; }
        header p { color: #666; font-size: 1.1em; max-width: 600px; margin: 0 auto 20px; }
        .contact-info a { 
            color: #0077ff; 
            text-decoration: none; 
            margin: 0 15px; 
            font-weight: bold;
            transition: color 0.2s;
        }
        .contact-info a:hover { color: #0056cc; }

        /* 核心：FlowUs裁剪容器（实现“只留视频区域”的关键） */
        .flowus-crop-wrapper {
            width: 100%;
            max-width: 1200px; /* 电脑端最大宽度，避免太宽 */
            margin: 0 auto 50px;
            padding: 0 20px;
            overflow: hidden; /* 核心：隐藏超出窗口的内容，实现裁剪 */
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            /* ========== 你要改的第1个参数：窗口高度 ========== */
            /* 数值=你要显示的视频区域总高度，多了会露底部多余内容，少了会裁掉视频 */
            height: 1600px; 
        }

        /* FlowUs嵌入iframe */
        .flowus-iframe {
            width: 100%;
            height: 2000px; /* 必须比上面的窗口高度大，才有裁剪空间 */
            border: none;
            /* ========== 你要改的第2个参数：向上偏移量 ========== */
            /* 数值越大，页面向上移的越多，裁掉的顶部内容越多 */
            transform: translateY(-120px); 
        }

        /* 手机端自动适配 */
        @media (max-width: 768px) {
            header h1 { font-size: 1.8em; }
            .flowus-crop-wrapper {
                height: 1800px; /* 手机端窗口高度，可单独微调 */
            }
            .flowus-iframe {
                transform: translateY(-100px); /* 手机端偏移量，可单独微调 */
            }
        }
    </style>
</head>
<body>

    <!-- 1. 个人信息栏，改成你自己的内容 -->
    <header>
        <h1>埃尔路德</h1>
        <p>专注游戏内容剪辑 | 擅长节奏把控、剧情向混剪与视觉叙事</p>
        <div class="contact-info">
            <a href="https://space.bilibili.com/你的B站ID" target="_blank">B站主页</a>
            <a href="https://www.douyin.com/user/你的抖音ID" target="_blank">抖音主页</a>
            <a href="mailto:你的邮箱@example.com">联系邮箱</a>
        </div>
    </header>

    <!-- 2. 核心：裁剪后的FlowUs视频嵌入区 -->
    <div class="flowus-crop-wrapper">
        <iframe 
            class="flowus-iframe"
            src="https://flowus.cn/aierlude/share/2f9e2b7a-5002-4168-a906-86f4bccc0615?code=EHYUZ7&embed=true"
            allowfullscreen="true"
            scrolling="no"
        ></iframe>
    </div>

</body>
</html>
