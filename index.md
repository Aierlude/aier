<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>埃尔路德 - 剪辑作品集</title>
    <style>
        /* 全局样式 - 简洁风 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: "PingFang SC", "Microsoft YaHei", sans-serif; background-color: #f9f9f9; color: #333; line-height: 1.6; }
        
        /* 头部个人信息 */
        header { background: #fff; padding: 40px 20px; text-align: center; box-shadow: 0 2px 10px rgba(0,0,0,0.05); }
        header h1 { font-size: 2.5em; margin-bottom: 10px; color: #222; }
        header p { color: #666; font-size: 1.1em; max-width: 600px; margin: 0 auto; }
        .contact-info { margin-top: 20px; }
        .contact-info a { color: #0077ff; text-decoration: none; margin: 0 10px; font-weight: bold; }

        /* 作品网格布局 */
        .container { max-width: 1200px; margin: 40px auto; padding: 0 20px; }
        .portfolio-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 25px; }
        
        /* 视频卡片样式 */
        .video-card { background: #fff; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 15px rgba(0,0,0,0.08); transition: transform 0.3s ease; cursor: pointer; }
        .video-card:hover { transform: translateY(-5px); }
        
        /* 封面图 */
        .thumbnail-wrapper { position: relative; width: 100%; padding-top: 177.78%; /* 9:16 比例，适合竖屏抖音 */ overflow: hidden; background: #eee; }
        .thumbnail-wrapper img { position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; }
        
        /* 播放按钮装饰 */
        .play-btn { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 50px; height: 50px; background: rgba(0,0,0,0.6); border-radius: 50%; display: flex; align-items: center; justify-content: center; opacity: 0; transition: opacity 0.3s; }
        .play-btn::after { content: ''; border-left: 15px solid #fff; border-top: 10px solid transparent; border-bottom: 10px solid transparent; margin-left: 5px; }
        .video-card:hover .play-btn { opacity: 1; }

        /* 视频信息 */
        .video-info { padding: 20px; }
        .video-title { font-size: 1.1em; font-weight: bold; color: #222; margin-bottom: 8px; }
        .video-desc { font-size: 0.9em; color: #777; }
    </style>
</head>
<body>

    <!-- 1. 个人信息区域 (请在此处修改) -->
    <header>
        <h1>埃尔路德</h1>
        <p>专注于游戏/魔兽内容剪辑 | 擅长节奏把控与视觉叙事</p>
        <div class="contact-info">
            <a href="https://space.bilibili.com/你的B站ID" target="_blank">B站主页</a>
            <a href="mailto:your-email@example.com">联系邮箱</a>
        </div>
    </header>

    <!-- 2. 作品展示区域 -->
    <div class="container">
        <div class="portfolio-grid" id="portfolio-grid">
            <!-- 卡片将通过 JS 自动生成，你只需要在下面的 script 中填写数据 -->
        </div>
    </div>

    <!-- 3. 数据填写区 (在这里添加你的视频链接) -->
    <script>
        // 你的作品集数据数组
        const myVideos = [
            {
                title: "魔兽世界：怀旧服精彩PVP集锦",
                description: "节奏向剪辑 | 耗时30小时",
                coverUrl: "https://picsum.photos/400/700?random=1", // 替换为你的封面图链接
                videoUrl: "https://www.douyin.com/video/你的抖音视频ID" // 替换为抖音链接
            },
            {
                title: "艾尔登法环：BOSS战混剪",
                description: "高燃踩点 | 电影级运镜",
                coverUrl: "https://picsum.photos/400/700?random=2",
                videoUrl: "https://www.douyin.com/video/你的抖音视频ID"
            },
            {
                title: "独立游戏开发日志",
                description: "Vlog式记录 | 角色展示篇",
                coverUrl: "https://picsum.photos/400/700?random=3",
                videoUrl: "https://www.douyin.com/video/你的抖音视频ID"
            }
            // 在这里按照格式继续添加更多...
        ];

        // 渲染逻辑 (不需要修改)
        const grid = document.getElementById('portfolio-grid');
        myVideos.forEach(video => {
            const card = document.createElement('a');
            card.href = video.videoUrl;
            card.target = "_blank";
            card.className = "video-card";
            card.innerHTML = `
                <div class="thumbnail-wrapper">
                    <img src="${video.coverUrl}" alt="${video.title}" loading="lazy">
                    <div class="play-btn"></div>
                </div>
                <div class="video-info">
                    <div class="video-title">${video.title}</div>
                    <div class="video-desc">${video.description}</div>
                </div>
            `;
            grid.appendChild(card);
        });
    </script>
</body>
</html>
