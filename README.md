<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Gesture Chess Game</title>
    <!-- 체스판 스타일 및 라이브러리 로드 -->
    <link rel="stylesheet" href="https://unpkg.com">
    <script src="https://jquery.com"></script>
    <script src="https://cloudflare.com"></script>
    <script src="https://unpkg.com"></script>
    
    <!-- MediaPipe 손 인식 라이브러리 로드 -->
    <script src="https://jsdelivr.net" crossorigin="anonymous"></script>
    <script src="https://jsdelivr.net" crossorigin="anonymous"></script>

    <style>
        body { display: flex; font-family: sans-serif; justify-content: center; align-items: center; height: 100vh; margin: 0; background: #222; color: white; }
        .container { display: flex; gap: 20px; }
        #board { width: 500px; }
        .video-container { position: relative; width: 400px; height: 300px; }
        #webcam { transform: scaleX(-1); width: 100%; height: 100%; border-radius: 8px; background: #333; }
        #gesture-status { margin-top: 10px; font-size: 1.2rem; font-weight: bold; text-align: center; }
    </style>
</head>
<body>

<div class="container">
    <!-- 체스판 영역 -->
    <div>
        <div id="board"></div>
    </div>
    
    <!-- 카메라 및 제스처 인식 영역 -->
    <div>
        <div class="video-container">
            <video id="webcam" autoplay playsinline></video>
        </div>
        <div id="gesture-status">제스처를 대기 중입니다...</div>
    </div>
</div>

<script src="game.js"></script>
</body>
</html>
