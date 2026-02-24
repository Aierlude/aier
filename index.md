<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>埃尔路德 - 剪辑作品集</title>
    <style>
        /* 全局基础样式 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; /* 平滑滚动效果 */ }
        body { 
            font-family: "PingFang SC", "Microsoft YaHei", sans-serif; 
            background-color: #f9f9f9; 
            color: #333; 
            line-height: 1.6;
            min-height: 100vh; /* 保证页面至少有一屏高度 */
            display: flex;
            flex-direction: column;
        }
        
        /* 应聘必备：个人信息头部 */
        header { 
            background: #fff; 
            padding: 80px 20px; 
            text-align: center; 
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            flex: 1; /* 让头部撑满剩余空间 */
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        header h1 { font-size: 3em; margin-bottom: 15px; color: #222; }
        header p { color: #666; font-size: 1.2em; max-width: 600px; margin: 0 auto 30px; }
        .contact-info { margin-bottom: 40px; }
        .contact-info a { 
            color: #0077ff; 
            text-decoration: none; 
            margin: 0 15px; 
            font-weight: bold;
            transition: color 0.2s;
        }
        .contact-info a:hover { color: #0056cc; }

        /* 手动查看按钮 */
        .view-works-btn {
            display: inline-block;
            padding: 15px 40px;
            background-color: #222;
            color: #fff;
            text-decoration: none;
            font-size: 1.1em;
            font-weight: bold;
            border-radius: 50px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        .view-works-btn:hover {
            background-color: #0077ff;
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0,119,255,0.3);
        }

        /* 视频区域标题 */
        .section-title {
            text-align: center;
            padding: 40px 20px 20px;
            font-size: 1.8em;
            color: #222;
        }

        /* 核心：FlowUs裁剪容器 */
        .flowus-crop-wrapper {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto 80px; /* 底部留更多空白 */
            padding: 0 20px;
            overflow: hidden;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            /* ========== 你要改的第1个参数：窗口高度 ========== */
            height: 1600px; 
        }

        /* FlowUs嵌入iframe */
        .flowus-iframe {
            width: 100%;
            height: 2000px;
            border: none;
            /* ========== 你要改的第2个参数：向上偏移量 ========== */
            transform: translateY(-120px); 
        }

        /* 手机端自动适配 */
        @media (max-width: 768px) {
            header { padding: 60px 20px; }
            header h1 { font-size: 2em; }
            .flowus-crop-wrapper {
                height: 1800px;
            }
            .flowus-iframe {
                transform: translateY(-100px);
            }
        }
    </style>
</head>
<body>

    <!-- 1. 个人信息栏（第一屏） -->
    <header>
        <h1>埃尔路德</h1>
        <p>专注游戏内容剪辑 | 擅长节奏把控、剧情向混剪与视觉叙事</p>
        <div class="contact-info">
            <a href="https://space.bilibili.com/你的B站ID" target="_blank">B站主页</a>
            <a href="https://www.douyin.com/user/你的抖音ID" target="_blank">抖音主页</a>
            <a href="mailto:你的邮箱@example.com">联系邮箱</a>
        </div>
        <!-- 手动按钮：点击后平滑滚动到底部视频区 -->
        <a href="#works-section" class="view-works-btn">查看我的剪辑作品</a>
    </header>

    <!-- 2. 视频区域（页面底部，通过锚点定位） -->
    <div id="works-section">
        <h2 class="section-title">作品展示</h2>
        <div class="flowus-crop-wrapper">
            <iframe 
                class="flowus-iframe"
                src="https://flowus.cn/aierlude/share/2f9e2b7a-5002-4168-a906-86f4bccc0615?code=EHYUZ7&embed=true"
                allowfullscreen="true"
                scrolling="no"
            ></iframe>
        </div>
    </div>

</body>
</html>
