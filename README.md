<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PNG to GIF Switcher</title>
    <style>
        img {
            width: 100%;
            max-width: 500px; /* 이미지 크기 조정 */
            cursor: pointer; /* 클릭 가능한 커서 표시 */
        }
    </style>
</head>
<body>
    <!-- PNG 이미지 -->
    <img id="switchImage" 
         src="https://drive.google.com/uc?id=1ILtHfyVLoYXRoDavDVmAzjwadpuE0hSD" 
         alt="PNG 이미지" />

    <script>
        const switchImage = document.getElementById('switchImage');

        // PNG와 GIF 링크 설정
        const pngImage = "https://drive.google.com/uc?id=1ILtHfyVLoYXRoDavDVmAzjwadpuE0hSD";
        const gifImage = "https://drive.google.com/uc?id=106ZAGcmHHvSXN66xQa3i37f0aiS5LmMk";

        // 클릭 이벤트
        switchImage.addEventListener('click', () => {
            // GIF로 변경
            switchImage.src = gifImage;

            // 35초 후 다시 PNG로 복구
            setTimeout(() => {
                switchImage.src = pngImage;
            }, 35000); // 35초 = 35000ms
        });
    </script>
</body>
</html>
