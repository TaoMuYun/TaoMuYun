<img align="right" src="https://count.getloli.com/get/@:QcxFlora?theme=rule3445594408">

## 普通在读学生—伯希Boxy

热爱绘画、热爱折腾。学习经验15年。喜欢参与一些开源项目的讨论。

### **社交：**
<img align="right" src="output.gif">



-   <img src="https://gimg3.baidu.com/search/src=https%3A%2F%2Fgameplus-platform.cdn.bcebos.com%2Fgameplus-platform%2Fupload%2Ffile%2Fimg%2Ffad44df25ce28a8e46a3c45ba8897393%2Ffad44df25ce28a8e46a3c45ba8897393.png&refer=http%3A%2F%2Fwww.baidu.com&app=2021&size=w931&n=0&g=0n&er=404&q=75&fmt=auto&maxorilen2heic=2000000?sec=1750179600&t=d14e6938ca28801b1bee032c50033dbf" style="height: 18px; width: 18px; border-radius: 50%; margin-right: 6px; object-fit: cover;" /><a href="https://ak.hypergryph.com/">卧槽粥!
-   >UID:585991431
-   <img src="https://gimg3.baidu.com/search/src=https%3A%2F%2Fapp-center.cdn.bcebos.com%2Fappcenter%2Fsts%2Fpcfile%2F646948909%2Fa5447c5cdb454c77935ce3fa2293d1ed.png&refer=http%3A%2F%2Fwww.baidu.com&app=2021&size=w150&n=0&g=0n&er=404&q=100&fmt=auto&maxorilen2heic=2000000?sec=1750179600&t=09fc3585200dedb0ffa0086dd9c677de" style="height: 18px; width: 18px; border-radius: 50%; margin-right: 6px; object-fit: cover;" /><a href="https://qm.qq.com/q/J3ZFM6Snee">我的QQ
-   >3445594408
-   <img src="https://pp.myapp.com/ma_icon/0/icon_240284_1749776149/96" style="height: 18px; width: 18px; border-radius: 50%; margin-right: 6px; object-fit: cover;" /><a href="mailto:boxy2699@163.com">我的邮箱
-   > boxy2699@163.com

### **今日份美图**
<img align="right" src="https://api.kxzjoker.cn/api/wallhere?type=bs">

### **今日份视频**
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>动态视频预览</title>
    <style>
        .video-preview {
            width: 300px;
            height: auto;
            cursor: pointer;
            border: 2px solid #ccc;
            border-radius: 8px;
        }
        .video-preview:hover {
            opacity: 0.8;
        }
        .error-message {
            color: red;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <img class="video-preview" id="videoPreview" alt="视频预览">
    <div id="errorMessage" class="error-message"></div>
    <script>
        const apiUrl = 'https://v2.api-m.com/api/meinv?return=302';

        // 获取视频第一帧
        async function getVideoFirstFrame(videoSrc) {
            return new Promise((resolve, reject) => {
                const video = document.createElement('video');
                video.src = videoSrc;
                video.crossOrigin = 'anonymous'; // 处理跨域
                video.muted = true;

                video.addEventListener('loadeddata', () => {
                    const canvas = document.createElement('canvas');
                    canvas.width = video.videoWidth;
                    canvas.height = video.videoHeight;
                    const ctx = canvas.getContext('2d');
                    ctx.drawImage(video, 0, 0, canvas.width, canvas.height);
                    resolve(canvas.toDataURL('image/png'));
                });

                video.addEventListener('error', () => {
                    reject('无法加载视频');
                });

                video.load();
            });
        }

        // 从 API 获取动态视频 URL
        async function fetchVideoUrl() {
            try {
                const response = await fetch(apiUrl, { method: 'GET', redirect: 'follow' });
                if (!response.ok) throw new Error('API 请求失败');
                // 假设 API 返回的是直接的视频 URL 或重定向后的 URL
                // 如果 API 返回 JSON，需解析相应字段，例如：response.json().videoUrl
                return response.url; // 获取重定向后的 URL
            } catch (error) {
                throw new Error('获取视频 URL 失败: ' + error.message);
            }
        }

        // 设置预览图和跳转
        async function setupVideoPreview() {
            const imgElement = document.getElementById('videoPreview');
            const errorElement = document.getElementById('errorMessage');

            try {
                // 获取动态视频 URL
                const videoUrl = await fetchVideoUrl();
                // 生成视频第一帧
                const previewImage = await getVideoFirstFrame(videoUrl);
                imgElement.src = previewImage;

                // 点击跳转到动态视频 URL
                imgElement.addEventListener('click', () => {
                    window.location.href = videoUrl;
                });
            } catch (error) {
                console.error('错误:', error);
                errorElement.textContent = '无法加载视频预览，请稍后重试';
                imgElement.alt = '无法加载预览图';
            }
        }

        // 初始化
        setupVideoPreview();
    </script>
</body>
</html>
<a href="http://cxk.fan/api.php">小黑子食不食油饼
