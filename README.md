<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>thpark5757의 시계</title>
    <style>
        body {
            background-color: #0f172a; /* 딥 다크 배경 */
            color: #38bdf8; /* 스카이 블루 포인트 */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: 'Courier New', Courier, monospace;
        }
        .clock-container {
            text-align: center;
        }
        #digital-clock {
            font-size: 8rem;
            font-weight: bold;
            text-shadow: 0 0 20px #38bdf8;
        }
        #date-display {
            font-size: 1.5rem;
            margin-top: 10px;
            color: #94a3b8;
        }
    </style>
</head>
<body>

    <div class="clock-container">
        <div id="digital-clock">00:00:00</div>
        <div id="date-display">YYYY-MM-DD</div>
    </div>

    <script>
        function updateClock() {
            const now = new Date();
            
            // 시간 포맷팅
            const h = String(now.getHours()).padStart(2, '0');
            const m = String(now.getHours()).padStart(2, '0'); // 오타 수정: m은 Minutes
            const s = String(now.getSeconds()).padStart(2, '0');
            
            // 날짜 포맷팅
            const year = now.getFullYear();
            const month = now.getMonth() + 1;
            const date = now.getDate();

            document.getElementById('digital-clock').innerText = `${h}:${String(now.getMinutes()).padStart(2, '0')}:${s}`;
            document.getElementById('date-display').innerText = `${year}년 ${month}월 ${date}일`;
        }

        setInterval(updateClock, 1000);
        updateClock(); // 즉시 실행
    </script>
</body>
</html>
