<!DOCTYPE html>
<html lang="zh-TW" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>羽極極限 - 專業羽球線上互動平台</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        badminton: {
                            light: '#eefc42',
                            DEFAULT: '#d4fc34', // 經典羽球螢光綠/黃
                            dark: '#a8cb1a',
                            darker: '#1e2911',
                        }
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    <!-- FontAwesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            font-family: 'Noto Sans TC', sans-serif;
            background-color: #0f172a; /* Slate 900 */
            color: #f1f5f9;
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a;
        }
        ::-webkit-scrollbar-thumb {
            background: #334155;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #d4fc34;
        }
    </style>
</head>
<body class="overflow-x-hidden">

    <!-- 導覽列 -->
    <nav class="fixed top-0 left-0 w-full z-50 bg-slate-900/90 backdrop-blur-md border-b border-slate-800 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16 sm:h-20">
                <div class="flex items-center gap-3">
                    <div class="bg-badminton text-slate-950 p-2 rounded-xl flex items-center justify-center font-black text-xl shadow-lg shadow-badminton/20 animate-pulse">
                        <i class="fa-solid fa-shuttlecock text-2xl rotate-45"></i>
                        <span class="ml-1 tracking-wider">ACE</span>
                    </div>
                    <span class="text-xl font-black tracking-widest bg-gradient-to-r from-white to-slate-400 bg-clip-text text-transparent">羽極領域</span>
                </div>
                
                <!-- 桌面端選單 -->
                <div class="hidden md:flex items-center gap-6">
                    <a href="#hero" class="text-slate-300 hover:text-badminton transition font-medium text-sm lg:text-base">首頁</a>
                    <a href="#booking" class="text-slate-300 hover:text-badminton transition font-medium text-sm lg:text-base">場地預約</a>
                    <a href="#scoreboard" class="text-slate-300 hover:text-badminton transition font-medium text-sm lg:text-base">專業記分板</a>
                    <a href="#tactics" class="text-slate-300 hover:text-badminton transition font-medium text-sm lg:text-base">互動戰術板</a>
                    <a href="#game" class="text-slate-300 hover:text-badminton transition font-medium text-sm lg:text-base">熱身小遊戲</a>
                </div>

                <!-- 行動端選單按鈕 -->
                <div class="md:hidden">
                    <button id="mobile-menu-btn" class="text-slate-400 hover:text-white focus:outline-none p-2">
                        <i class="fa-solid fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- 行動端下拉選單 -->
        <div id="mobile-menu" class="hidden md:hidden bg-slate-950/95 border-b border-slate-800 px-4 py-4 space-y-3 transition-all duration-300">
            <a href="#hero" class="block text-slate-300 hover:text-badminton py-2 border-b border-slate-800/50">首頁</a>
            <a href="#booking" class="block text-slate-300 hover:text-badminton py-2 border-b border-slate-800/50">場地預約</a>
            <a href="#scoreboard" class="block text-slate-300 hover:text-badminton py-2 border-b border-slate-800/50">專業記分板</a>
            <a href="#tactics" class="block text-slate-300 hover:text-badminton py-2 border-b border-slate-800/50">互動戰術板</a>
            <a href="#game" class="block text-slate-300 hover:text-badminton py-2">熱身小遊戲</a>
        </div>
    </nav>

    <!-- Hero 英雄主視覺 -->
    <section id="hero" class="relative min-h-screen pt-20 flex items-center justify-center overflow-hidden bg-gradient-to-b from-slate-950 via-slate-900 to-slate-950">
        <!-- 背景裝飾網格與光效 -->
        <div class="absolute inset-0 bg-[linear-gradient(to_right,#0f172a_1px,transparent_1px),linear-gradient(to_bottom,#0f172a_1px,transparent_1px)] bg-[size:4rem_4rem] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_50%,#000_70%,transparent_100%)] opacity-30"></div>
        <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-badminton/10 rounded-full blur-[120px] pointer-events-none"></div>
        <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-blue-500/10 rounded-full blur-[120px] pointer-events-none"></div>

        <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 text-center z-10">
            <span class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-badminton/10 text-badminton text-sm font-semibold tracking-wider uppercase mb-6 border border-badminton/20 animate-bounce">
                <i class="fa-solid fa-fire text-xs"></i> 2026 全新升級羽球線上管家
            </span>
            <h1 class="text-4xl sm:text-6xl lg:text-7xl font-black tracking-tight mb-6 leading-tight">
                掌握節奏，揮灑汗水<br>
                <span class="bg-gradient-to-r from-badminton via-teal-300 to-emerald-400 bg-clip-text text-transparent">引領羽球新紀元</span>
            </h1>
            <p class="text-lg sm:text-xl text-slate-400 max-w-3xl mx-auto mb-10 leading-relaxed">
                無論是尋找絕佳球場、在激烈對局中專業記分，還是與隊友佈置致勝戰術，我們提供您羽球運動所需的一切，一站式釋放您的無限潛能。
            </p>

            <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                <a href="#booking" class="w-full sm:w-auto px-8 py-4 bg-badminton text-slate-950 font-bold rounded-xl hover:bg-badminton-dark hover:scale-105 transition-all duration-300 shadow-lg shadow-badminton/35 text-center flex items-center justify-center gap-2">
                    <i class="fa-regular fa-calendar-check"></i> 立即線上預約場地
                </a>
                <a href="#game" class="w-full sm:w-auto px-8 py-4 bg-slate-800 text-white font-semibold rounded-xl hover:bg-slate-700 hover:scale-105 transition-all duration-300 text-center flex items-center justify-center gap-2 border border-slate-700">
                    <i class="fa-solid fa-gamepad"></i> 挑戰接羽球小遊戲
                </a>
            </div>

            <!-- 特色亮點卡片 -->
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6 mt-20 max-w-6xl mx-auto text-left">
                <div class="bg-slate-900/60 p-6 rounded-2xl border border-slate-800 hover:border-badminton/30 transition-all duration-300">
                    <div class="w-12 h-12 rounded-xl bg-badminton/10 flex items-center justify-center text-badminton text-xl mb-4">
                        <i class="fa-solid fa-map-location-dot"></i>
                    </div>
                    <h3 class="text-lg font-bold mb-2">智慧場地選擇</h3>
                    <p class="text-slate-400 text-sm">視覺化球場預約，一鍵選定最佳時段，防撞場最省心。</p>
                </div>
                <div class="bg-slate-900/60 p-6 rounded-2xl border border-slate-800 hover:border-badminton/30 transition-all duration-300">
                    <div class="w-12 h-12 rounded-xl bg-badminton/10 flex items-center justify-center text-badminton text-xl mb-4">
                        <i class="fa-solid fa-list-ol"></i>
                    </div>
                    <h3 class="text-lg font-bold mb-2">專業標準記分</h3>
                    <p class="text-slate-400 text-sm">自訂單雙打規則，計分簡潔流暢，賽後數據一眼掌握。</p>
                </div>
                <div class="bg-slate-900/60 p-6 rounded-2xl border border-slate-800 hover:border-badminton/30 transition-all duration-300">
                    <div class="w-12 h-12 rounded-xl bg-badminton/10 flex items-center justify-center text-badminton text-xl mb-4">
                        <i class="fa-solid fa-pen-ruler"></i>
                    </div>
                    <h3 class="text-lg font-bold mb-2">極簡互動戰術板</h3>
                    <p class="text-slate-400 text-sm">拖曳球員，自由勾勒進攻防守路線，臨場戰術一目了然。</p>
                </div>
                <div class="bg-slate-900/60 p-6 rounded-2xl border border-slate-800 hover:border-badminton/30 transition-all duration-300">
                    <div class="w-12 h-12 rounded-xl bg-badminton/10 flex items-center justify-center text-badminton text-xl mb-4">
                        <i class="fa-solid fa-ranking-star"></i>
                    </div>
                    <h3 class="text-lg font-bold mb-2">即時趣味熱身</h3>
                    <p class="text-slate-400 text-sm">擬真羽球重力物理學，動手挑戰高難度顛球紀錄！</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 1. 場地預約系統 -->
    <section id="booking" class="py-24 bg-slate-950 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl sm:text-4xl font-black mb-4">
                    <span class="text-badminton">01.</span> 線上智慧場地預約
                </h2>
                <p class="text-slate-400 max-w-xl mx-auto">精確挑選羽球場地，告別繁瑣排隊。點擊您心儀的時段和場地立即排程！</p>
            </div>

            <!-- 預約卡片面板 -->
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- 左側：條件篩選 -->
                <div class="bg-slate-900 rounded-3xl p-6 border border-slate-800 space-y-6">
                    <h3 class="text-xl font-bold flex items-center gap-2 text-white">
                        <i class="fa-solid fa-sliders text-badminton"></i> 篩選預約設定
                    </h3>
                    <hr class="border-slate-800">
                    
                    <div>
                        <label class="block text-sm font-semibold text-slate-400 mb-2">預約日期</label>
                        <input type="date" id="booking-date" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-badminton transition">
                    </div>

                    <div>
                        <label class="block text-sm font-semibold text-slate-400 mb-2">球場材質</label>
                        <select id="court-type" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-badminton transition">
                            <option value="all">全部材質 (木質地板 / 塑膠地墊)</option>
                            <option value="plastic">頂級 PVC 綠色塑膠地墊 (4面)</option>
                            <option value="wood">頂級楓木運動地板 (2面)</option>
                        </select>
                    </div>

                    <div class="bg-slate-950 p-4 rounded-xl border border-slate-800 space-y-3">
                        <span class="text-xs font-bold uppercase text-slate-500 block">圖例說明</span>
                        <div class="grid grid-cols-2 gap-2 text-xs">
                            <div class="flex items-center gap-2"><div class="w-3 h-3 bg-slate-800 rounded"></div> <span>已被預約</span></div>
                            <div class="flex items-center gap-2"><div class="w-3 h-3 bg-badminton rounded"></div> <span>您已選取</span></div>
                            <div class="flex items-center gap-2"><div class="w-3 h-3 bg-emerald-500 rounded"></div> <span>開放預約</span></div>
                            <div class="flex items-center gap-2"><div class="w-3 h-3 bg-amber-500 rounded"></div> <span>清潔保養中</span></div>
                        </div>
                    </div>
                </div>

                <!-- 右側：主預約區域 (場地與時段矩陣) -->
                <div class="lg:col-span-2 bg-slate-900 rounded-3xl p-6 border border-slate-800">
                    <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between mb-6 gap-4">
                        <div>
                            <h3 id="current-booking-date-title" class="text-xl font-bold">2026/05/27 場地狀況</h3>
                            <p class="text-xs text-slate-400">請選取單一時段和場地（每次限選一格進行預定）</p>
                        </div>
                        <div class="flex gap-2 text-xs">
                            <span class="px-3 py-1 bg-slate-800 text-slate-400 rounded-full">費率：NT$ 350 / 小時</span>
                        </div>
                    </div>

                    <!-- 橫向滑動容納表格 -->
                    <div class="overflow-x-auto">
                        <table class="w-full border-collapse text-left min-w-[600px]">
                            <thead>
                                <tr class="border-b border-slate-800">
                                    <th class="py-3 px-4 text-xs font-bold uppercase text-slate-400">時段 / 場地</th>
                                    <th class="py-3 px-4 text-xs font-bold uppercase text-slate-400 text-center">A 場 (塑膠)</th>
                                    <th class="py-3 px-4 text-xs font-bold uppercase text-slate-400 text-center">B 場 (塑膠)</th>
                                    <th class="py-3 px-4 text-xs font-bold uppercase text-slate-400 text-center">C 場 (木地板)</th>
                                    <th class="py-3 px-4 text-xs font-bold uppercase text-slate-400 text-center">D 場 (木地板)</th>
                                </tr>
                            </thead>
                            <tbody id="booking-grid" class="divide-y divide-slate-800/50">
                                <!-- 由 JS 動態生成場地狀態 -->
                            </tbody>
                        </table>
                    </div>

                    <!-- 預約確認提交區 -->
                    <div id="booking-confirm-panel" class="hidden mt-8 p-4 bg-slate-950 rounded-2xl border border-badminton/20 animate-fadeIn">
                        <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4">
                            <div>
                                <h4 class="font-bold text-badminton flex items-center gap-2">
                                    <i class="fa-solid fa-circle-check"></i> 確認預約內容
                                </h4>
                                <p id="booking-summary-text" class="text-sm text-slate-300 mt-1">
                                    預約 2026-05-27 | B場 (塑膠) | 14:00 - 15:00
                                </p>
                            </div>
                            <button id="submit-booking-btn" class="w-full sm:w-auto px-6 py-2.5 bg-badminton text-slate-950 font-bold rounded-xl hover:bg-badminton-dark transition-all">
                                送出預約
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 2. 專業記分板 -->
    <section id="scoreboard" class="py-24 bg-slate-900 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl sm:text-4xl font-black mb-4">
                    <span class="text-badminton">02.</span> 專業羽球計分板
                </h2>
                <p class="text-slate-400 max-w-xl mx-auto">專為標準羽毛球比賽設計的計分板。提供發球權自動提示、勝負判定及賽事紀錄。</p>
            </div>

            <!-- 計分板主控台 -->
            <div class="max-w-4xl mx-auto bg-slate-950 rounded-3xl p-6 sm:p-8 border border-slate-800 shadow-2xl">
                
                <!-- 計分板設定 & 重設 -->
                <div class="flex flex-wrap items-center justify-between gap-4 mb-6 pb-6 border-b border-slate-800">
                    <div class="flex items-center gap-4">
                        <select id="game-type" class="bg-slate-900 border border-slate-800 rounded-xl px-4 py-2 text-sm text-slate-300 focus:outline-none focus:border-badminton">
                            <option value="singles">單打賽 (1 v 1)</option>
                            <option value="doubles">雙打賽 (2 v 2)</option>
                        </select>
                        <select id="target-score" class="bg-slate-900 border border-slate-800 rounded-xl px-4 py-2 text-sm text-slate-300 focus:outline-none focus:border-badminton">
                            <option value="21">21 分制 (標準)</option>
                            <option value="11">11 分制 (練習)</option>
                        </select>
                    </div>
                    <div class="flex gap-2">
                        <button id="score-swap" class="px-3 py-2 bg-slate-900 text-slate-400 hover:text-white rounded-xl border border-slate-800 transition" title="交換方位">
                            <i class="fa-solid fa-arrows-rotate"></i>
                        </button>
                        <button id="score-reset" class="px-4 py-2 bg-rose-500/10 text-rose-400 hover:bg-rose-500/20 rounded-xl border border-rose-500/20 transition flex items-center gap-2">
                            <i class="fa-solid fa-rotate"></i> 重設戰局
                        </button>
                    </div>
                </div>

                <!-- 局數面板 (Sets/Games Tracker) -->
                <div class="flex items-center justify-center gap-8 mb-6 text-sm">
                    <div class="text-center">
                        <span class="text-slate-500 font-bold block mb-1">TEAM A 局數</span>
                        <div class="flex gap-1 justify-center" id="team-a-sets">
                            <span class="w-3 h-3 rounded-full bg-slate-800 transition-colors duration-300"></span>
                            <span class="w-3 h-3 rounded-full bg-slate-800 transition-colors duration-300"></span>
                        </div>
                    </div>
                    <div class="text-slate-600 font-bold text-xl px-4 border-x border-slate-800">局數統計 (三戰兩勝)</div>
                    <div class="text-center">
                        <span class="text-slate-500 font-bold block mb-1">TEAM B 局數</span>
                        <div class="flex gap-1 justify-center" id="team-b-sets">
                            <span class="w-3 h-3 rounded-full bg-slate-800 transition-colors duration-300"></span>
                            <span class="w-3 h-3 rounded-full bg-slate-800 transition-colors duration-300"></span>
                        </div>
                    </div>
                </div>

                <!-- 計分板核心 -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 relative">
                    <!-- 發球網中央裝飾線 -->
                    <div class="hidden md:block absolute left-1/2 top-0 bottom-0 w-px bg-dashed bg-slate-800"></div>

                    <!-- 隊伍 A (左側/上方) -->
                    <div class="bg-slate-900/60 rounded-2xl p-6 border-2 border-transparent hover:border-slate-800 transition text-center flex flex-col justify-between h-80 relative group">
                        <!-- 發球權指示器 -->
                        <div id="serve-a" class="absolute top-4 left-4 flex items-center gap-2 bg-badminton/10 text-badminton text-xs font-bold px-3 py-1 rounded-full border border-badminton/20 opacity-0 transition-opacity duration-300">
                            <i class="fa-solid fa-shuttlecock animate-bounce"></i> 發球中
                        </div>
                        <input type="text" value="TEAM A" class="bg-transparent border-b border-transparent hover:border-slate-700 focus:border-badminton focus:outline-none text-center font-bold text-lg text-slate-300 py-1 mx-auto max-w-[200px] uppercase">
                        
                        <div class="my-auto">
                            <!-- 分數主按鈕 -->
                            <button id="score-a-btn" class="text-8xl font-black text-white hover:text-badminton active:scale-95 transition-all outline-none select-none">0</button>
                        </div>

                        <div class="flex items-center justify-center gap-4">
                            <button id="minus-a-btn" class="w-8 h-8 rounded-full bg-slate-800 hover:bg-slate-700 text-slate-300 flex items-center justify-center text-sm transition">
                                <i class="fa-solid fa-minus"></i>
                            </button>
                            <span class="text-xs text-slate-500">點擊大數字得分 / 連點減分</span>
                        </div>
                    </div>

                    <!-- 隊伍 B (右側/下方) -->
                    <div class="bg-slate-900/60 rounded-2xl p-6 border-2 border-transparent hover:border-slate-800 transition text-center flex flex-col justify-between h-80 relative group">
                        <!-- 發球權指示器 -->
                        <div id="serve-b" class="absolute top-4 right-4 flex items-center gap-2 bg-badminton/10 text-badminton text-xs font-bold px-3 py-1 rounded-full border border-badminton/20 opacity-0 transition-opacity duration-300">
                            發球中 <i class="fa-solid fa-shuttlecock animate-bounce"></i>
                        </div>
                        <input type="text" value="TEAM B" class="bg-transparent border-b border-transparent hover:border-slate-700 focus:border-badminton focus:outline-none text-center font-bold text-lg text-slate-300 py-1 mx-auto max-w-[200px] uppercase">
                        
                        <div class="my-auto">
                            <!-- 分數主按鈕 -->
                            <button id="score-b-btn" class="text-8xl font-black text-white hover:text-badminton active:scale-95 transition-all outline-none select-none">0</button>
                        </div>

                        <div class="flex items-center justify-center gap-4">
                            <button id="minus-b-btn" class="w-8 h-8 rounded-full bg-slate-800 hover:bg-slate-700 text-slate-300 flex items-center justify-center text-sm transition">
                                <i class="fa-solid fa-minus"></i>
                            </button>
                            <span class="text-xs text-slate-500">點擊大數字得分 / 連點減分</span>
                        </div>
                    </div>
                </div>

                <!-- 比賽事件紀錄 / 局數歷史 -->
                <div class="mt-8 bg-slate-900/50 p-4 rounded-2xl border border-slate-800">
                    <h4 class="text-sm font-bold text-slate-400 mb-3 flex items-center gap-2">
                        <i class="fa-solid fa-history text-xs text-badminton"></i> 局數分數歷程
                    </h4>
                    <div class="grid grid-cols-3 gap-2 text-center text-sm font-semibold" id="set-history-list">
                        <div class="p-3 bg-slate-950 rounded-xl border border-slate-800">
                            <span class="text-xs text-slate-500 block mb-1">第一局 (Game 1)</span>
                            <span id="g1-score" class="text-slate-400">-</span>
                        </div>
                        <div class="p-3 bg-slate-950 rounded-xl border border-slate-800">
                            <span class="text-xs text-slate-500 block mb-1">第二局 (Game 2)</span>
                            <span id="g2-score" class="text-slate-400">-</span>
                        </div>
                        <div class="p-3 bg-slate-950 rounded-xl border border-slate-800">
                            <span class="text-xs text-slate-500 block mb-1">第三局 (Game 3)</span>
                            <span id="g3-score" class="text-slate-400">-</span>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 3. 互動戰術板 -->
    <section id="tactics" class="py-24 bg-slate-950 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl sm:text-4xl font-black mb-4">
                    <span class="text-badminton">03.</span> 即時互動羽球戰術板
                </h2>
                <p class="text-slate-400 max-w-xl mx-auto">拖曳球員標記到指定位置，使用畫筆即時繪製發球路線、跑位路徑，打造致勝戰術。</p>
            </div>

            <div class="max-w-5xl mx-auto grid grid-cols-1 lg:grid-cols-4 gap-8">
                <!-- 戰術工具欄 -->
                <div class="bg-slate-900 rounded-3xl p-6 border border-slate-800 space-y-6 flex flex-col justify-between h-auto">
                    <div class="space-y-6">
                        <h3 class="text-lg font-bold flex items-center gap-2">
                            <i class="fa-solid fa-toolbox text-badminton"></i> 戰術工具箱
                        </h3>
                        <hr class="border-slate-800">

                        <!-- 畫筆設定 -->
                        <div>
                            <span class="block text-sm text-slate-400 font-bold mb-2">1. 選擇畫筆顏色</span>
                            <div class="flex gap-3">
                                <button class="paint-color-btn w-10 h-10 rounded-full border-2 border-white bg-amber-400 shadow-md transform scale-110" data-color="#f59e0b"></button>
                                <button class="paint-color-btn w-10 h-10 rounded-full border-2 border-transparent bg-rose-500 shadow-md" data-color="#f43f5e"></button>
                                <button class="paint-color-btn w-10 h-10 rounded-full border-2 border-transparent bg-sky-400 shadow-md" data-color="#38bdf8"></button>
                                <button class="paint-color-btn w-10 h-10 rounded-full border-2 border-transparent bg-badminton shadow-md" data-color="#d4fc34"></button>
                            </div>
                        </div>

                        <!-- 筆觸大小 -->
                        <div>
                            <span class="block text-sm text-slate-400 font-bold mb-2">2. 筆觸粗細</span>
                            <input type="range" id="brush-size" min="2" max="15" value="5" class="w-full accent-badminton">
                        </div>

                        <!-- 清除功能 -->
                        <div class="grid grid-cols-1 gap-2 pt-2">
                            <button id="clear-draw" class="w-full py-2.5 bg-slate-800 hover:bg-slate-700 text-slate-200 rounded-xl transition flex items-center justify-center gap-2 border border-slate-700">
                                <i class="fa-solid fa-eraser"></i> 清除手繪軌跡
                            </button>
                            <button id="reset-tactics" class="w-full py-2.5 bg-rose-500/10 text-rose-400 hover:bg-rose-500/20 border border-rose-500/20 rounded-xl transition flex items-center justify-center gap-2">
                                <i class="fa-solid fa-arrows-to-dot"></i> 還原初始站位
                            </button>
                        </div>
                    </div>

                    <div class="p-4 bg-slate-950 rounded-2xl border border-slate-800 text-xs text-slate-400 space-y-2">
                        <span class="font-bold text-slate-300 block">操作小提醒：</span>
                        <p>• 可直接在右方場地上按住滑鼠或觸控以繪製軌跡。</p>
                        <p>• 球員頭像 (A1/A2/B1/B2/球) 可自由拖曳移動。</p>
                    </div>
                </div>

                <!-- 羽球場與球員 (主要畫布區) -->
                <div class="lg:col-span-3 bg-slate-900 rounded-3xl p-6 border border-slate-800 flex flex-col items-center">
                    
                    <!-- 自訂戰術板容器 (Relative 以便絕對定位球員頭像) -->
                    <div id="tactics-court-wrapper" class="relative w-full aspect-[4/6] max-w-[420px] bg-emerald-800 rounded-2xl border-4 border-white shadow-2xl overflow-hidden select-none touch-none">
                        
                        <!-- 畫布：用於手繪軌跡 -->
                        <canvas id="tactics-canvas" class="absolute inset-0 z-10 w-full h-full cursor-crosshair"></canvas>

                        <!-- 羽球場線條 (CSS / 模擬真實場地) -->
                        <div class="absolute inset-x-0 inset-y-0 pointer-events-none border-2 border-white/80">
                            <!-- 左右雙打邊線 -->
                            <div class="absolute left-[5%] right-[5%] top-0 bottom-0 border-x-2 border-white/60"></div>
                            <!-- 後發球線 (雙打) -->
                            <div class="absolute inset-x-0 top-[8%] bottom-[8%] border-y-2 border-white/60"></div>
                            <!-- 網子位置線 -->
                            <div class="absolute inset-x-0 top-1/2 h-[3px] bg-slate-300 flex items-center justify-center">
                                <span class="bg-slate-700 text-[10px] px-2 text-white/80 rounded-full scale-75 uppercase font-bold tracking-widest border border-white/20">Net 網前</span>
                            </div>
                            <!-- 前發球線 (單/雙打) -->
                            <div class="absolute inset-x-0 top-[35%] bottom-[35%] border-y-2 border-white/60"></div>
                            <!-- 中線 -->
                            <div class="absolute left-1/2 top-0 bottom-[35%] w-[2px] bg-white/60 -translate-x-1/2"></div>
                            <div class="absolute left-1/2 bottom-0 top-[65%] w-[2px] bg-white/60 -translate-x-1/2"></div>
                        </div>

                        <!-- 拖曳物件：球員與羽毛球 -->
                        <!-- A隊 (上方) -->
                        <div class="tactics-token absolute z-20 w-10 h-10 rounded-full bg-blue-600 text-white border-2 border-white flex items-center justify-center font-black text-sm shadow-lg cursor-grab active:cursor-grabbing" id="token-a1" style="top: 15%; left: 30%;">A1</div>
                        <div class="tactics-token absolute z-20 w-10 h-10 rounded-full bg-blue-600 text-white border-2 border-white flex items-center justify-center font-black text-sm shadow-lg cursor-grab active:cursor-grabbing" id="token-a2" style="top: 15%; left: 60%;">A2</div>

                        <!-- B隊 (下方) -->
                        <div class="tactics-token absolute z-20 w-10 h-10 rounded-full bg-rose-600 text-white border-2 border-white flex items-center justify-center font-black text-sm shadow-lg cursor-grab active:cursor-grabbing" id="token-b1" style="top: 75%; left: 30%;">B1</div>
                        <div class="tactics-token absolute z-20 w-10 h-10 rounded-full bg-rose-600 text-white border-2 border-white flex items-center justify-center font-black text-sm shadow-lg cursor-grab active:cursor-grabbing" id="token-b2" style="top: 75%; left: 60%;">B2</div>

                        <!-- 羽球標記 -->
                        <div class="tactics-token absolute z-30 w-8 h-8 rounded-full bg-badminton text-slate-950 border-2 border-slate-950 flex items-center justify-center font-black text-xs shadow-xl cursor-grab active:cursor-grabbing" id="token-ball" style="top: 47%; left: 45%;">
                            <i class="fa-solid fa-shuttlecock text-[10px]"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. 熱身小遊戲：羽球接空接 (Canvas Physics Game) -->
    <section id="game" class="py-24 bg-slate-900 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl sm:text-4xl font-black mb-4">
                    <span class="text-badminton">04.</span> 羽球顛球熱身挑戰賽
                </h2>
                <p class="text-slate-400 max-w-xl mx-auto">
                    使用球拍將球不斷頂起！滑鼠或觸控滑動控制羽球拍。球拍接觸時會賦予反彈力，看看您最高能顛球幾下！
                </p>
            </div>

            <!-- 遊戲主體 -->
            <div class="max-w-3xl mx-auto bg-slate-950 rounded-3xl p-6 border border-slate-800 flex flex-col items-center">
                
                <!-- 控制與分數顯示 -->
                <div class="w-full flex items-center justify-between mb-4 px-2">
                    <div class="flex items-center gap-6">
                        <div>
                            <span class="text-xs text-slate-500 font-bold block">目前分數</span>
                            <span id="game-current-score" class="text-2xl font-black text-badminton">0</span>
                        </div>
                        <div>
                            <span class="text-xs text-slate-500 font-bold block">最佳紀錄</span>
                            <span id="game-high-score" class="text-2xl font-black text-white">0</span>
                        </div>
                    </div>
                    <button id="game-start-btn" class="px-6 py-2.5 bg-badminton text-slate-950 font-bold rounded-xl hover:bg-badminton-dark active:scale-95 transition-all flex items-center gap-2 shadow-lg shadow-badminton/10">
                        <i class="fa-solid fa-play"></i> 開始遊戲
                    </button>
                </div>

                <!-- 遊戲畫布容器 -->
                <div class="relative w-full max-w-[500px] aspect-[4/5] bg-slate-900 rounded-2xl border-2 border-slate-800 overflow-hidden shadow-inner">
                    <canvas id="game-canvas" class="w-full h-full block cursor-none"></canvas>
                    
                    <!-- 遊戲未開始/結束蓋板 -->
                    <div id="game-overlay" class="absolute inset-0 bg-slate-950/80 backdrop-blur-sm flex flex-col items-center justify-center text-center p-6 transition-all duration-300">
                        <div class="w-20 h-20 bg-badminton/10 border-2 border-badminton text-badminton rounded-full flex items-center justify-center text-3xl mb-4 animate-bounce">
                            <i class="fa-solid fa-shuttlecock rotate-45"></i>
                        </div>
                        <h3 id="game-overlay-title" class="text-2xl font-black mb-2 text-white">準備好揮拍了嗎？</h3>
                        <p id="game-overlay-desc" class="text-slate-400 text-sm max-w-xs mb-6">點擊上方「開始遊戲」按鈕，將游標移動至畫布內控制綠色羽球拍，不要讓羽毛球墜地！</p>
                        <button id="game-overlay-btn" class="px-8 py-3 bg-badminton text-slate-950 font-bold rounded-xl hover:bg-badminton-dark transition-all">
                            立即啟動
                        </button>
                    </div>
                </div>

                <div class="w-full text-center mt-4 text-xs text-slate-500">
                    * 貼心提示：羽毛球會因重力自然下落。撞擊球拍側邊或偏角會造成不規則彈跳，考驗您的控球極限！
                </div>
            </div>
        </div>
    </section>

    <!-- Footer 頁尾 -->
    <footer class="bg-slate-950 border-t border-slate-900 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-6">
            <div class="flex items-center justify-center gap-3">
                <div class="bg-badminton text-slate-950 p-2 rounded-xl flex items-center justify-center font-black text-lg">
                    <i class="fa-solid fa-shuttlecock text-lg rotate-45"></i>
                </div>
                <span class="text-lg font-black tracking-widest text-white">羽極領域</span>
            </div>
            <p class="text-xs text-slate-500 max-w-md mx-auto leading-relaxed">
                © 2026 ACE Badminton Club. 保留所有權利。專業網頁架構、球場數據分析與頂級羽球管家服務。
            </p>
            <div class="flex justify-center gap-4 text-slate-500 text-sm">
                <a href="#" class="hover:text-badminton transition">服務條款</a>
                <span>•</span>
                <a href="#" class="hover:text-badminton transition">隱私政策</a>
                <span>•</span>
                <a href="#" class="hover:text-badminton transition">技術支援</a>
            </div>
        </div>
    </footer>

    <!-- 通知訊息彈窗 (取代 alert) -->
    <div id="toast-message" class="fixed bottom-6 right-6 z-50 transform translate-y-20 opacity-0 bg-slate-900 border-2 border-badminton text-white px-6 py-4 rounded-2xl shadow-2xl flex items-center gap-3 transition-all duration-300 max-w-sm">
        <div class="w-8 h-8 rounded-full bg-badminton/20 text-badminton flex items-center justify-center text-sm">
            <i class="fa-solid fa-bell"></i>
        </div>
        <div>
            <span id="toast-title" class="font-bold block text-sm">系統提示</span>
            <span id="toast-desc" class="text-xs text-slate-400">這是一條即時提示訊息。</span>
        </div>
    </div>


    <!-- ============================================== -->
    <!-- JavaScript 邏輯控制與系統串接 -->
    <!-- ============================================== -->
    <script>
        // --- 核心共用元件與Toast系統 ---
        const toast = {
            show: function(title, desc, duration = 3000) {
                const toastEl = document.getElementById('toast-message');
                document.getElementById('toast-title').textContent = title;
                document.getElementById('toast-desc').textContent = desc;
                
                toastEl.classList.remove('translate-y-20', 'opacity-0');
                toastEl.classList.add('translate-y-0', 'opacity-100');
                
                setTimeout(() => {
                    toastEl.classList.remove('translate-y-0', 'opacity-100');
                    toastEl.classList.add('translate-y-20', 'opacity-0');
                }, duration);
            }
        };

        // 行動端選單展開收合
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });


        // ==============================================
        // 1. 場地預約系統邏輯
        // ==============================================
        const bookingDateInput = document.getElementById('booking-date');
        const bookingGrid = document.getElementById('booking-grid');
        const bookingConfirmPanel = document.getElementById('booking-confirm-panel');
        const bookingSummaryText = document.getElementById('booking-summary-text');
        const submitBookingBtn = document.getElementById('submit-booking-btn');
        const currentBookingDateTitle = document.getElementById('current-booking-date-title');

        // 設定今日為預設日期
        const today = new Date().toISOString().split('T')[0];
        bookingDateInput.value = today;
        bookingDateInput.min = today;

        // 模擬場地預訂狀態 (Key: Date_Time_Court)
        const mockBookingState = {
            [`${today}_09:00-10:00_courtA`]: 'booked',
            [`${today}_10:00-11:00_courtA`]: 'booked',
            [`${today}_10:00-11:00_courtB`]: 'booked',
            [`${today}_14:00-15:00_courtD`]: 'maintenance',
            [`${today}_15:00-16:00_courtC`]: 'booked',
        };

        let activeSelection = null; // 紀錄目前玩家選取：{ date, time, courtCode, courtName }

        function renderBookingGrid() {
            const selectedDate = bookingDateInput.value;
            currentBookingDateTitle.textContent = `${selectedDate} 場地狀況`;
            bookingGrid.innerHTML = '';

            const timeSlots = [
                '09:00 - 10:00',
                '10:00 - 11:00',
                '11:00 - 12:00',
                '13:00 - 14:00',
                '14:00 - 15:00',
                '15:00 - 16:00',
                '16:00 - 17:00',
                '18:00 - 19:00',
                '19:00 - 20:00',
                '20:00 - 21:00'
            ];

            const courts = [
                { id: 'courtA', name: 'A 場 (塑膠)' },
                { id: 'courtB', name: 'B 場 (塑膠)' },
                { id: 'courtC', name: 'C 場 (木地板)' },
                { id: 'courtD', name: 'D 場 (木地板)' }
            ];

            timeSlots.forEach(slot => {
                const tr = document.createElement('tr');
                tr.className = 'hover:bg-slate-900 transition-colors border-b border-slate-800/40';

                // 時段標題
                const tdTime = document.createElement('td');
                tdTime.className = 'py-4 px-4 text-sm font-bold text-slate-300';
                tdTime.textContent = slot;
                tr.appendChild(tdTime);

                // 每一面場地
                courts.forEach(court => {
                    const td = document.createElement('td');
                    td.className = 'py-2 px-2 text-center';

                    const stateKey = `${selectedDate}_${slot.replace(/\s+/g, '')}_${court.id}`;
                    const bookingStatus = mockBookingState[stateKey] || 'available';

                    const btn = document.createElement('button');
                    btn.className = 'w-full py-2.5 rounded-xl font-bold text-xs transition duration-200 focus:outline-none';

                    if (bookingStatus === 'booked') {
                        btn.textContent = '已被預約';
                        btn.className += ' bg-slate-800 text-slate-500 cursor-not-allowed';
                        btn.disabled = true;
                    } else if (bookingStatus === 'maintenance') {
                        btn.textContent = '保養中';
                        btn.className += ' bg-amber-500/10 text-amber-500 border border-amber-500/20 cursor-not-allowed';
                        btn.disabled = true;
                    } else {
                        // 檢查此格是否正被選中
                        const isCurrentSelection = activeSelection &&
                            activeSelection.date === selectedDate &&
                            activeSelection.time === slot &&
                            activeSelection.courtCode === court.id;

                        if (isCurrentSelection) {
                            btn.textContent = '您的選擇';
                            btn.className += ' bg-badminton text-slate-950 ring-2 ring-badminton/30';
                        } else {
                            btn.textContent = '預約';
                            btn.className += ' bg-emerald-500/10 text-emerald-400 hover:bg-emerald-500 hover:text-slate-950 border border-emerald-500/20';
                        }

                        btn.addEventListener('click', () => {
                            selectCourtSlot(selectedDate, slot, court.id, court.name);
                        });
                    }

                    td.appendChild(btn);
                    tr.appendChild(td);
                });

                bookingGrid.appendChild(tr);
            });
        }

        function selectCourtSlot(date, time, courtCode, courtName) {
            // 如果重複點擊則取消
            if (activeSelection && activeSelection.date === date && activeSelection.time === time && activeSelection.courtCode === courtCode) {
                activeSelection = null;
                bookingConfirmPanel.classList.add('hidden');
            } else {
                activeSelection = { date, time, courtCode, courtName };
                bookingSummaryText.textContent = `您已選取：${date} ｜ ${courtName} ｜ ${time}`;
                bookingConfirmPanel.classList.remove('hidden');
            }
            renderBookingGrid();
        }

        // 提交預約
        submitBookingBtn.addEventListener('click', () => {
            if (!activeSelection) return;
            const { date, time, courtCode, courtName } = activeSelection;
            const stateKey = `${date}_${time.replace(/\s+/g, '')}_${courtCode}`;

            // 將預訂狀態存為已定
            mockBookingState[stateKey] = 'booked';
            
            toast.show(
                '預約成功！', 
                `已為您預約 ${date} 的 ${courtName} (${time})`
            );

            activeSelection = null;
            bookingConfirmPanel.classList.add('hidden');
            renderBookingGrid();
        });

        // 監聽日期與材質更動
        bookingDateInput.addEventListener('change', () => {
            activeSelection = null;
            bookingConfirmPanel.classList.add('hidden');
            renderBookingGrid();
        });

        document.getElementById('court-type').addEventListener('change', (e) => {
            // 在此模擬篩選：簡單透過 UI 顏色展示或提示篩選結果
            toast.show('篩選成功', `正在顯示 ${e.target.selectedOptions[0].text}`);
        });

        // 預設載入預約網格
        renderBookingGrid();


        // ==============================================
        // 2. 專業記分板邏輯
        // ==============================================
        const scoreState = {
            teamA: { name: 'TEAM A', score: 0, sets: 0 },
            teamB: { name: 'TEAM B', score: 0, sets: 0 },
            server: 'A', // A 或 B
            targetScore: 21,
            gameType: 'singles',
            setHistory: [],
            currentSet: 1
        };

        const scoreABtn = document.getElementById('score-a-btn');
        const scoreBBtn = document.getElementById('score-b-btn');
        const minusABtn = document.getElementById('minus-a-btn');
        const minusBBtn = document.getElementById('minus-b-btn');
        const serveAIndicator = document.getElementById('serve-a');
        const serveBIndicator = document.getElementById('serve-b');
        const scoreResetBtn = document.getElementById('score-reset');
        const scoreSwapBtn = document.getElementById('score-swap');

        function updateScoreboardUI() {
            scoreABtn.textContent = scoreState.teamA.score;
            scoreBBtn.textContent = scoreState.teamB.score;

            // 局數圓點亮起控制
            const teamASetDots = document.querySelectorAll('#team-a-sets span');
            const teamBSetDots = document.querySelectorAll('#team-b-sets span');

            teamASetDots.forEach((dot, idx) => {
                if (idx < scoreState.teamA.sets) {
                    dot.classList.add('bg-badminton');
                    dot.classList.remove('bg-slate-800');
                } else {
                    dot.classList.remove('bg-badminton');
                    dot.classList.add('bg-slate-800');
                }
            });

            teamBSetDots.forEach((dot, idx) => {
                if (idx < scoreState.teamB.sets) {
                    dot.classList.add('bg-badminton');
                    dot.classList.remove('bg-slate-800');
                } else {
                    dot.classList.remove('bg-badminton');
                    dot.classList.add('bg-slate-800');
                }
            });

            // 發球權指示器亮起
            if (scoreState.server === 'A') {
                serveAIndicator.classList.remove('opacity-0');
                serveBIndicator.classList.add('opacity-0');
            } else {
                serveAIndicator.classList.add('opacity-0');
                serveBIndicator.classList.remove('opacity-0');
            }

            // 更新局數歷程
            for (let i = 1; i <= 3; i++) {
                const cell = document.getElementById(`g${i}-score`);
                if (scoreState.setHistory[i - 1]) {
                    cell.textContent = `${scoreState.setHistory[i - 1].A} : ${scoreState.setHistory[i - 1].B}`;
                    cell.className = 'text-badminton font-bold text-base';
                } else {
                    if (scoreState.currentSet === i) {
                        cell.textContent = '進行中';
                        cell.className = 'text-white italic text-xs animate-pulse';
                    } else {
                        cell.textContent = '-';
                        cell.className = 'text-slate-400';
                    }
                }
            }
        }

        // 行動端發球邏輯與分數判定
        function recordScore(pointWinner) {
            // 加分
            if (pointWinner === 'A') {
                scoreState.teamA.score++;
                scoreState.server = 'A';
            } else {
                scoreState.teamB.score++;
                scoreState.server = 'B';
            }

            checkSetWinner();
            updateScoreboardUI();
        }

        function decreaseScore(pointLoser) {
            if (pointLoser === 'A' && scoreState.teamA.score > 0) {
                scoreState.teamA.score--;
            } else if (pointLoser === 'B' && scoreState.teamB.score > 0) {
                scoreState.teamB.score--;
            }
            updateScoreboardUI();
        }

        function checkSetWinner() {
            const target = scoreState.targetScore;
            const sA = scoreState.teamA.score;
            const sB = scoreState.teamB.score;

            // 羽毛球標準規則：先拿到 21 分。若領先不足 2 分則進入 Deuce（追分至領先 2 分或最高 30 分先得者勝）
            const maxScore = 30;

            let isSetEnded = false;
            let winner = null;

            if (sA >= target || sB >= target) {
                if (Math.abs(sA - sB) >= 2) {
                    winner = sA > sB ? 'A' : 'B';
                    isSetEnded = true;
                } else if (sA === maxScore || sB === maxScore) {
                    winner = sA === maxScore ? 'A' : 'B';
                    isSetEnded = true;
                }
            }

            if (isSetEnded) {
                // 將目前比分存入歷史紀錄
                scoreState.setHistory.push({ A: sA, B: sB });
                
                if (winner === 'A') {
                    scoreState.teamA.sets++;
                    toast.show('局數結束！', `TEAM A 獲得第 ${scoreState.currentSet} 局勝利！`);
                } else {
                    scoreState.teamB.sets++;
                    toast.show('局數結束！', `TEAM B 獲得第 ${scoreState.currentSet} 局勝利！`);
                }

                // 檢查是否贏得整場比賽
                if (scoreState.teamA.sets === 2 || scoreState.teamB.sets === 2) {
                    const finalWinner = scoreState.teamA.sets === 2 ? 'TEAM A' : 'TEAM B';
                    toast.show('🏆 全場結束 🏆', `${finalWinner} 拿下 2 局，贏得最終大捷！`, 5000);
                    // 鎖定分數並提供清空按鈕
                } else {
                    // 繼續下一局
                    scoreState.currentSet++;
                }

                // 重設單局分數
                scoreState.teamA.score = 0;
                scoreState.teamB.score = 0;
            }
        }

        // 綁定記分板按鈕事件
        scoreABtn.addEventListener('click', () => recordScore('A'));
        scoreBBtn.addEventListener('click', () => recordScore('B'));
        minusABtn.addEventListener('click', () => decreaseScore('A'));
        minusBBtn.addEventListener('click', () => decreaseScore('B'));

        scoreResetBtn.addEventListener('click', () => {
            scoreState.teamA.score = 0;
            scoreState.teamB.score = 0;
            scoreState.teamA.sets = 0;
            scoreState.teamB.sets = 0;
            scoreState.server = 'A';
            scoreState.setHistory = [];
            scoreState.currentSet = 1;
            updateScoreboardUI();
            toast.show('重設成功', '所有比分已歸零，比賽重新開始。');
        });

        scoreSwapBtn.addEventListener('click', () => {
            // 交換畫面上 A / B 隊伍的分數（模擬換場）
            const temp = scoreState.teamA;
            scoreState.teamA = scoreState.teamB;
            scoreState.teamB = temp;
            
            // 同時交換發球權
            scoreState.server = scoreState.server === 'A' ? 'B' : 'A';

            updateScoreboardUI();
            toast.show('更換場地', '雙方方位已進行互換。');
        });

        // 局數規則/單雙打設定變動
        document.getElementById('target-score').addEventListener('change', (e) => {
            scoreState.targetScore = parseInt(e.target.value);
            toast.show('規則變動', `目標比分調整為 ${scoreState.targetScore} 分`);
        });

        document.getElementById('game-type').addEventListener('change', (e) => {
            scoreState.gameType = e.target.value;
            toast.show('模式調整', `已更換為 ${e.target.value === 'singles' ? '單打' : '雙打'} 比賽`);
        });

        // 初始化更新 UI
        updateScoreboardUI();


        // ==============================================
        // 3. 互動戰術板邏輯
        // ==============================================
        const canvas = document.getElementById('tactics-canvas');
        const ctx = canvas.getContext('2d');
        const brushSizeInput = document.getElementById('brush-size');
        const clearDrawBtn = document.getElementById('clear-draw');
        const resetTacticsBtn = document.getElementById('reset-tactics');
        const tokens = document.querySelectorAll('.tactics-token');
        const courtWrapper = document.getElementById('tactics-court-wrapper');

        let isDrawing = false;
        let lastX = 0;
        let lastY = 0;
        let brushColor = '#f59e0b'; // 預設琥珀橙色
        let brushSize = 5;

        // 響應畫布大小
        function resizeTacticsCanvas() {
            canvas.width = courtWrapper.clientWidth;
            canvas.height = courtWrapper.clientHeight;
            ctx.lineCap = 'round';
            ctx.lineJoin = 'round';
        }

        window.addEventListener('resize', resizeTacticsCanvas);
        // 初始化畫布大小
        setTimeout(resizeTacticsCanvas, 100);

        // 畫筆控制
        document.querySelectorAll('.paint-color-btn').forEach(btn => {
            btn.addEventListener('click', (e) => {
                document.querySelectorAll('.paint-color-btn').forEach(b => b.classList.remove('border-white', 'scale-110'));
                e.target.classList.add('border-white', 'scale-110');
                brushColor = e.target.dataset.color;
            });
        });

        brushSizeInput.addEventListener('input', (e) => {
            brushSize = e.target.value;
        });

        // 畫筆觸發事件
        function getCanvasMousePos(e) {
            const rect = canvas.getBoundingClientRect();
            // 相容 touch 與 mouse 事件
            const clientX = e.touches ? e.touches[0].clientX : e.clientX;
            const clientY = e.touches ? e.touches[0].clientY : e.clientY;
            return {
                x: clientX - rect.left,
                y: clientY - rect.top
            };
        }

        function startDrawing(e) {
            // 如果是在拖曳球員，則不觸發畫筆
            if (e.target.classList.contains('tactics-token')) return;
            isDrawing = true;
            const pos = getCanvasMousePos(e);
            lastX = pos.x;
            lastY = pos.y;
        }

        function draw(e) {
            if (!isDrawing) return;
            e.preventDefault();
            const pos = getCanvasMousePos(e);

            ctx.beginPath();
            ctx.moveTo(lastX, lastY);
            ctx.lineTo(pos.x, pos.y);
            ctx.strokeStyle = brushColor;
            ctx.lineWidth = brushSize;
            ctx.stroke();

            lastX = pos.x;
            lastY = pos.y;
        }

        function stopDrawing() {
            isDrawing = false;
        }

        // 綁定畫布手寫觸碰
        canvas.addEventListener('mousedown', startDrawing);
        canvas.addEventListener('mousemove', draw);
        window.addEventListener('mouseup', stopDrawing);

        canvas.addEventListener('touchstart', startDrawing);
        canvas.addEventListener('touchmove', draw);
        window.addEventListener('touchend', stopDrawing);

        // 清除與還原
        clearDrawBtn.addEventListener('click', () => {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            toast.show('畫布清空', '已擦除所有的繪圖軌跡。');
        });

        const initialTokenPositions = {
            'token-a1': { top: '15%', left: '30%' },
            'token-a2': { top: '15%', left: '60%' },
            'token-b1': { top: '75%', left: '30%' },
            'token-b2': { top: '75%', left: '60%' },
            'token-ball': { top: '47%', left: '45%' }
        };

        resetTacticsBtn.addEventListener('click', () => {
            Object.keys(initialTokenPositions).forEach(id => {
                const el = document.getElementById(id);
                el.style.top = initialTokenPositions[id].top;
                el.style.left = initialTokenPositions[id].left;
            });
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            toast.show('戰術板重設', '球員站位已恢復初始狀態。');
        });

        // 拖曳（Token Drag and Drop）原生支援 (滑鼠與觸控)
        tokens.forEach(token => {
            token.addEventListener('mousedown', (e) => startDrag(e, token));
            token.addEventListener('touchstart', (e) => startDrag(e, token), { passive: false });
        });

        function startDrag(e, token) {
            e.preventDefault();
            const rect = courtWrapper.getBoundingClientRect();
            
            function moveAt(clientX, clientY) {
                // 將位置轉換為百分比，保持 RWD 彈性
                const x = clientX - rect.left - token.offsetWidth / 2;
                const y = clientY - rect.top - token.offsetHeight / 2;
                
                // 限制在球場邊框內
                const xPercent = Math.max(0, Math.min(100 - (token.offsetWidth / rect.width) * 100, (x / rect.width) * 100));
                const yPercent = Math.max(0, Math.min(100 - (token.offsetHeight / rect.height) * 100, (y / rect.height) * 100));
                
                token.style.left = `${xPercent}%`;
                token.style.top = `${yPercent}%`;
            }

            function onMouseMove(moveEvent) {
                const clientX = moveEvent.touches ? moveEvent.touches[0].clientX : moveEvent.clientX;
                const clientY = moveEvent.touches ? moveEvent.touches[0].clientY : moveEvent.clientY;
                moveAt(clientX, clientY);
            }

            // 初始化時觸發一次
            const initialX = e.touches ? e.touches[0].clientX : e.clientX;
            const initialY = e.touches ? e.touches[0].clientY : e.clientY;
            moveAt(initialX, initialY);

            // 綁定事件監聽
            document.addEventListener('mousemove', onMouseMove);
            document.addEventListener('touchmove', onMouseMove, { passive: false });

            // 釋放事件
            function stopDrag() {
                document.removeEventListener('mousemove', onMouseMove);
                document.removeEventListener('touchmove', onMouseMove);
                document.removeEventListener('mouseup', stopDrag);
                document.removeEventListener('touchend', stopDrag);
            }

            document.addEventListener('mouseup', stopDrag);
            document.addEventListener('touchend', stopDrag);
        }


        // ==============================================
        // 4. 熱身小遊戲 (Canvas Badminton Game)
        // ==============================================
        const gameCanvas = document.getElementById('game-canvas');
        const gameCtx = gameCanvas.getContext('2d');
        const gameOverlay = document.getElementById('game-overlay');
        const gameOverlayTitle = document.getElementById('game-overlay-title');
        const gameOverlayDesc = document.getElementById('game-overlay-desc');
        const gameOverlayBtn = document.getElementById('game-overlay-btn');
        const gameStartBtn = document.getElementById('game-start-btn');
        const gameCurrentScoreText = document.getElementById('game-current-score');
        const gameHighScoreText = document.getElementById('game-high-score');

        let isPlaying = false;
        let gameLoopId = null;
        let currentScore = 0;
        let highScore = 0;

        // 羽球物件
        const shuttle = {
            x: 0,
            y: 0,
            radius: 12,
            vx: 0,
            vy: 0,
            gravity: 0.16,
            drag: 0.99, // 羽球空氣阻力，提供慢速飄浮感
            rotation: 0
        };

        // 球拍物件
        const racket = {
            x: 0,
            y: 0,
            width: 75,
            height: 12,
            prevX: 0, // 用於計算橫向揮拍加速度
            prevY: 0
        };

        // 適配遊戲畫布大小
        function resizeGameCanvas() {
            const container = gameCanvas.parentElement;
            gameCanvas.width = container.clientWidth;
            gameCanvas.height = container.clientHeight;
        }

        window.addEventListener('resize', resizeGameCanvas);
        resizeGameCanvas();

        // 綁定鼠標/觸控與球拍同步
        function updateRacketPos(clientX, clientY) {
            const rect = gameCanvas.getBoundingClientRect();
            racket.prevX = racket.x;
            racket.prevY = racket.y;
            // 球拍中心對齊游標
            racket.x = clientX - rect.left;
            racket.y = clientY - rect.top;

            // 限制球拍在畫布邊界
            if (racket.x < racket.width / 2) racket.x = racket.width / 2;
            if (racket.x > gameCanvas.width - racket.width / 2) racket.x = gameCanvas.width - racket.width / 2;
        }

        gameCanvas.addEventListener('mousemove', (e) => {
            if (!isPlaying) return;
            updateRacketPos(e.clientX, e.clientY);
        });

        gameCanvas.addEventListener('touchmove', (e) => {
            if (!isPlaying) return;
            e.preventDefault();
            const touch = e.touches[0];
            updateRacketPos(touch.clientX, touch.clientY);
        }, { passive: false });

        // 開始/重新開始遊戲
        function startGame() {
            if (gameLoopId) cancelAnimationFrame(gameLoopId);
            
            // 重設參數
            currentScore = 0;
            gameCurrentScoreText.textContent = currentScore;
            
            shuttle.x = gameCanvas.width / 2;
            shuttle.y = 80;
            shuttle.vx = (Math.random() - 0.5) * 4;
            shuttle.vy = 2; // 初速向下
            
            isPlaying = true;
            gameOverlay.classList.add('hidden');
            gameStartBtn.innerHTML = `<i class="fa-solid fa-rotate"></i> 重新開始`;
            
            gameLoop();
        }

        function endGame() {
            isPlaying = false;
            cancelAnimationFrame(gameLoopId);
            
            if (currentScore > highScore) {
                highScore = currentScore;
                gameHighScoreText.textContent = highScore;
                toast.show('🎉 創造紀錄！', `恭喜您顛球了 ${highScore} 下！寫下了個人最新里程碑。`, 4000);
            } else {
                toast.show('挑戰結束', `本次獲得 ${currentScore} 分！再試一次吧！`);
            }

            gameOverlayTitle.textContent = "落地失敗！";
            gameOverlayDesc.textContent = `別氣餒！您這次顛球了 ${currentScore} 下。調整重心與拍面，下一次必定大獲全勝！`;
            gameOverlayBtn.textContent = "再次挑戰";
            gameOverlay.classList.remove('hidden');
        }

        // 遊戲循環核心
        function gameLoop() {
            if (!isPlaying) return;

            // 1. 清空畫布
            gameCtx.clearRect(0, 0, gameCanvas.width, gameCanvas.height);

            // 2. 羽毛球物理演算 (考慮空氣阻力與重力)
            shuttle.vy += shuttle.gravity;
            shuttle.vx *= shuttle.drag;
            shuttle.vy *= shuttle.drag;
            shuttle.x += shuttle.vx;
            shuttle.y += shuttle.vy;

            // 計算羽毛球的旋轉 (根據其速度方向，頭部通常朝下/朝前)
            shuttle.rotation = Math.atan2(shuttle.vy, shuttle.vx) + Math.PI / 2;

            // 3. 牆壁邊界彈射
            if (shuttle.x - shuttle.radius < 0) {
                shuttle.x = shuttle.radius;
                shuttle.vx *= -0.8; // 輕微彈力損失
            } else if (shuttle.x + shuttle.radius > gameCanvas.width) {
                shuttle.x = gameCanvas.width - shuttle.radius;
                shuttle.vx *= -0.8;
            }

            // 4. 判定羽毛球落地
            if (shuttle.y - shuttle.radius > gameCanvas.height) {
                endGame();
                return;
            }

            // 5. 判定羽毛球碰撞球拍 (Racket Collision Check)
            const rxLeft = racket.x - racket.width / 2;
            const rxRight = racket.x + racket.width / 2;
            const ryTop = racket.y - racket.height / 2;
            const ryBottom = racket.y + racket.height / 2;

            // 精細碰撞檢測
            if (shuttle.x + shuttle.radius > rxLeft && 
                shuttle.x - shuttle.radius < rxRight && 
                shuttle.y + shuttle.radius > ryTop && 
                shuttle.y - shuttle.radius < ryBottom) {
                
                // 只有羽毛球向下或平移時才能擊起
                if (shuttle.vy > 0) {
                    shuttle.y = ryTop - shuttle.radius; // 防穿透修正

                    // 計算撞擊位置 (擊球中心點偏移量)
                    const hitOffset = (shuttle.x - racket.x) / (racket.width / 2); // 介於 -1 ~ 1
                    
                    // 動態施加縱向速度與橫向偏向力
                    shuttle.vy = -6.5 - Math.abs(racket.y - racket.prevY) * 0.3; // 依據揮拍速度施加反彈力
                    shuttle.vx += hitOffset * 3.5 + (racket.x - racket.prevX) * 0.2; // 橫向切球

                    // 得分加算
                    currentScore++;
                    gameCurrentScoreText.textContent = currentScore;
                    
                    // 隨機反彈音效特效 (閃爍特效)
                    gameCanvas.classList.add('bg-badminton/10');
                    setTimeout(() => gameCanvas.classList.remove('bg-badminton/10'), 60);
                }
            }

            // 6. 繪製球拍
            gameCtx.save();
            gameCtx.shadowColor = 'rgba(212, 252, 52, 0.4)';
            gameCtx.shadowBlur = 10;
            
            // 握把 (下段)
            gameCtx.fillStyle = '#475569';
            gameCtx.fillRect(racket.x - 3, racket.y + racket.height / 2, 6, 25);
            
            // 拍面
            const racketGrad = gameCtx.createLinearGradient(rxLeft, 0, rxRight, 0);
            racketGrad.addColorStop(0, '#a8cb1a');
            racketGrad.addColorStop(0.5, '#d4fc34');
            racketGrad.addColorStop(1, '#a8cb1a');
            gameCtx.fillStyle = racketGrad;
            
            // 繪製圓角矩形拍面
            gameCtx.beginPath();
            gameCtx.roundRect(rxLeft, ryTop, racket.width, racket.height, 6);
            gameCtx.fill();
            gameCtx.restore();


            // 7. 繪製羽毛球 (採用手動精緻 SVG 風格渲染，而非僅僅是圓球)
            gameCtx.save();
            gameCtx.translate(shuttle.x, shuttle.y);
            gameCtx.rotate(shuttle.rotation);

            // 羽球白裙 (羽毛)
            gameCtx.fillStyle = 'rgba(248, 250, 252, 0.85)';
            gameCtx.beginPath();
            gameCtx.moveTo(0, 10); // 球頭中心偏下
            gameCtx.lineTo(-12, -22); // 左裙邊
            gameCtx.lineTo(12, -22);  // 右裙邊
            gameCtx.closePath();
            gameCtx.fill();

            // 羽毛條紋雕刻
            gameCtx.strokeStyle = 'rgba(148, 163, 184, 0.5)';
            gameCtx.lineWidth = 1.5;
            gameCtx.beginPath();
            gameCtx.moveTo(-6, -8); gameCtx.lineTo(-8, -22);
            gameCtx.moveTo(0, -6); gameCtx.lineTo(0, -22);
            gameCtx.moveTo(6, -8); gameCtx.lineTo(8, -22);
            gameCtx.stroke();

            // 頂部羽翼橫線
            gameCtx.beginPath();
            gameCtx.arc(0, -14, 9, Math.PI, 0, false);
            gameCtx.stroke();

            // 羽球頭 (綠色/黑條交接膠帶 + 軟木球頭)
            gameCtx.fillStyle = '#d4fc34'; // 螢光軟木塞
            gameCtx.beginPath();
            gameCtx.arc(0, 8, shuttle.radius, Math.PI, 0, true);
            gameCtx.fill();

            // 軟木塞黑色線段 (連接裙部)
            gameCtx.fillStyle = '#0f172a';
            gameCtx.fillRect(-shuttle.radius, 1, shuttle.radius * 2, 3);

            gameCtx.restore();

            // 繼續下一幀
            gameLoopId = requestAnimationFrame(gameLoop);
        }

        // 綁定遊戲按鈕
        gameStartBtn.addEventListener('click', startGame);
        gameOverlayBtn.addEventListener('click', startGame);
    </script>
</body>
</html>
