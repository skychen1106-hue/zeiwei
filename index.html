<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>天空紫微 x 核心抽籤系統</title>
    <style>
        /* 全域設定 */
        html, body { height: 100%; margin: 0; padding: 0; background-color: #f4f4f9; font-family: "Microsoft JhengHei", sans-serif; display: flex; flex-direction: column; color: #333; }
        
        /* 標題區 */
        .header { background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d); color: white; padding: 20px 0; text-align: center; box-shadow: 0 2px 10px rgba(0,0,0,0.2); }
        h1 { margin: 0; font-size: 22px; letter-spacing: 2px; }

        /* 主要內容區 */
        .main-content { flex-grow: 1; display: flex; flex-direction: column; align-items: center; padding: 20px; box-sizing: border-box; overflow-y: auto; }
        
        /* 說明文字區 */
        .info-section { width: 100%; max-width: 500px; background: white; border-radius: 8px; padding: 15px; margin-bottom: 20px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        .info-section h2 { font-size: 16px; margin-top: 0; color: #b21f1f; border-bottom: 1px solid #eee; padding-bottom: 5px; }
        .info-section ul, .info-section ol { padding-left: 20px; font-size: 14px; line-height: 1.6; }

        /* 結果顯示區 */
        #result-display { 
            width: 100%; 
            max-width: 500px; 
            min-height: 120px; 
            background: #fff; 
            border: 2px dashed #ccc; 
            border-radius: 15px; 
            display: flex; 
            flex-direction: column; 
            align-items: center; 
            justify-content: center; 
            margin-bottom: 20px;
            transition: all 0.3s;
        }
        .result-title { font-size: 14px; color: #888; margin-bottom: 10px; }
        .result-text { font-size: 32px; font-weight: bold; color: #d42424; text-shadow: 1px 1px 2px rgba(0,0,0,0.1); }

        /* 按鈕群組 */
        .btn-group { width: 100%; max-width: 500px; display: grid; grid-template-columns: 1fr; gap: 12px; margin-bottom: 30px; }
        .draw-btn { 
            border: none; 
            border-radius: 50px; 
            padding: 15px; 
            font-size: 18px; 
            font-weight: bold; 
            color: white; 
            cursor: pointer; 
            box-shadow: 0 4px 6px rgba(0,0,0,0.1); 
            transition: transform 0.1s; 
        }
        .draw-btn:active { transform: scale(0.95); }
        
        /* 按鈕顏色區分 */
        .btn-main { background-color: #8b0000; } /* 深紅 */
        .btn-assist { background-color: #2c3e50; } /* 深藍 */
        .btn-life { background-color: #27ae60; } /* 綠色 */

        #loading { display: none; font-weight: bold; color: #b21f1f; margin-bottom: 10px; animation: blink 1s infinite; }
        @keyframes blink { 0% { opacity: 1; } 50% { opacity: 0.5; } 100% { opacity: 1; } }
    </style>
</head>
<body>

    <div class="header"><h1>✨ 天空紫微核心系統 ✨</h1></div>

    <div class="main-content">
        <div id="result-display">
            <div class="result-title">請誠心祈禱後選擇籤筒</div>
            <div class="result-text" id="output">尚未抽籤</div>
        </div>

        <p id="loading">正在請示神靈...</p>

        <div class="btn-group">
            <button class="draw-btn btn-main" onclick="draw('main')">【主星牌組】點此抽籤</button>
            <button class="draw-btn btn-assist" onclick="draw('assist')">【輔星牌組】點此抽籤</button>
            <button class="draw-btn btn-life" onclick="draw('life')">【十二長生牌】點此抽籤</button>
        </div>

        <div class="info-section">
            <h2>📜 抽牌前準備</h2>
            <ol>
                <li><strong>清淨心神：</strong>深呼吸，讓思緒平靜。</li>
                <li><strong>聚焦問題：</strong>清晰思考你想請示的問題。</li>
            </ol>
        </div>
        <div class="info-section">
            <h2>⚠️ 抽牌禁忌</h2>
            <ul>
                <li><strong>一事不二問：</strong>同一件事短期內不要重複。</li>
                <li><strong>不可問惡事：</strong>不可請示不道德之事務。</li>
                <li><strong>真心誠意：</strong>不可嬉鬧，誠懇面對。</li>
            </ul>
        </div>
    </div>

    <script>
        // 資料庫設定
        const decks = {
            main: [
                "紫微星", "紫微天府雙星", "紫微天相雙星", "紫微破軍雙星", "紫微七殺雙星", "紫微貪狼雙星",
                "天府星", "天相星", "天梁星", "七殺星", "破軍星", "貪狼星", "巨門星", "巨門太陽雙星",
                "太陽星", "太陽天梁雙星", "太陽太陰雙星", "太陰星", "太陰天同雙星", "天同星",
                "天同巨門雙星", "天同天梁雙星", "天機星", "天機巨門雙星", "天機天梁雙星", "天機太陰雙星",
                "武曲天府雙星", "武曲天相雙星", "武曲破軍雙星", "武曲七殺雙星", "武曲貪狼雙星",
                "廉貞星", "廉貞天府雙星", "廉貞天相雙星", "廉貞破軍雙星", "廉貞七殺雙星", "廉貞貪狼雙星", "空宮牌"
            ],
            assist: [
                "紅鸞", "天喜", "左輔", "右弼", "文昌", "文曲", "天魁", "天鉞", "擎羊", "陀羅",
                "鈴星", "火星", "地空", "地劫", "祿存", "天馬", "化忌", "化祿", "化權", "化科"
            ],
            life: [
                "長生", "沐浴", "冠帶", "臨官", "帝旺", "衰", "病", "死", "墓", "絕", "胎", "養"
            ]
        };

        const output = document.getElementById('output');
        const loading = document.getElementById('loading');
        const resultDisplay = document.getElementById('result-display');

        function draw(type) {
            // 顯示載入中動畫
            loading.style.display = 'block';
            output.style.opacity = '0.3';
            
            // 模擬請示時間 (0.5秒後出結果)
            setTimeout(() => {
                const deck = decks[type];
                const randomIndex = Math.floor(Math.random() * deck.length);
                const result = deck[randomIndex];

                // 更新文字與樣式
                output.innerText = result;
                output.style.opacity = '1';
                loading.style.display = 'none';

                // 根據類型微調邊框顏色
                if(type === 'main') resultDisplay.style.borderColor = '#8b0000';
                if(type === 'assist') resultDisplay.style.borderColor = '#2c3e50';
                if(type === 'life') resultDisplay.style.borderColor = '#27ae60';

                // 手機震動反饋 (若手機支援)
                if (window.navigator.vibrate) {
                    window.navigator.vibrate(50);
                }
            }, 500);
        }
    </script>
</body>
</html>
