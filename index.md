<!DOCTYPE html>
<html>
   <head>
       <title>"埃尔路德"</title>
       <meta charset="utf-8">

   </head>
   <body>
      
     <a href="https://flowus.cn/aierlude/share/c3cdaab3-cc41-44b7-a23c-c3afe6875380?code=EHYUZ7 " target="_blank">" 埃尔路德官网www.aierlude.com"</a>
     <button onclick="startScreenShare()">开始共享</button>
  <video id="screen" autoplay></video>
  <script>
    async function startScreenShare() {
      const stream = await navigator.mediaDevices.getDisplayMedia({ video: true, audio: true });
      const video = document.getElementById('screen');
      video.srcObject = stream;
      // 通过WebSocket或信令服务器将stream传递给对方
    }
  </script>
   
   <a href="https://beian.miit.gov.cn/ " target="_blank">" 备案"</a>
      
   </body>
 </html>
