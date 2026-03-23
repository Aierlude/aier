<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>个人作品集</title>
<style>
    /* 基础重置，确保没有默认边距 */
    body { margin: 0; padding: 0; background-color: #f7f9fc; font-family: sans-serif; }

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
        box-sizing: border-box;
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

    <header>
        <h1>你的名字 / 求职意向</h1>
        <p>简单的一句话自我介绍，或者说明这个作品集的重点内容。</p>
        <div class="contact-info">
            <a href="#">邮箱：your@email.com</a>
            <a href="#">电话：138xxxx0000</a>
        </div>
    </header>

    <div class="flowus-crop-wrapper">
        <iframe 
            class="flowus-iframe" 
            src="https://flowus.cn/aierlude/share/c3cdaab3-cc41-44b7-a23c-c3afe6875380?code=EHYUZ7&embed=true" 
            allowfullscreen>
        </iframe>
    </div>

</body>
</html>
