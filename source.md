Preview
Code
Fact check content
Select to edit
Copy<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            font-family: 'Roboto', sans-serif;
        }
        .slide {
            width: 1280px;
            min-height: 720px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            position: relative;
            overflow: hidden;
        }
        .slide::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 400px;
            height: 400px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transform: translate(200px, -200px);
        }
        .slide::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 300px;
            height: 300px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transform: translate(-150px, 150px);
        }
        .title {
            font-size: 3.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 2rem;
            line-height: 1.2;
            max-width: 80%;
            z-index: 1;
        }
        .subtitle {
            font-size: 1.8rem;
            font-weight: 300;
            text-align: center;
            margin-bottom: 3rem;
            color: rgba(255, 255, 255, 0.9);
            z-index: 1;
        }
        .date {
            font-size: 1.4rem;
            font-weight: 400;
            color: rgba(255, 255, 255, 0.8);
            z-index: 1;
        }
        .forex-icon {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: rgba(255, 255, 255, 0.9);
            z-index: 1;
        }
    </style>
</head>
<body>
    <div class="slide">
        <i class="fas fa-chart-line forex-icon"></i>
        <h1 class="title">Как успешно проходить проп-трейдинг на рынке Forex в 2025 году</h1>
        <h2 class="subtitle">Стратегии и рекомендации для трейдеров</h2>
        <div class="date">Апрель 2025</div>
    </div>
</body>
</html>
1 / 7
Preview
Code
Fact check content
Select to edit
Copy<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            font-family: 'Roboto', sans-serif;
            color: white;
        }
        .slide {
            width: 1280px;
            min-height: 720px;
            margin: 0 auto;
            padding: 40px;
        }
        .title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
        }
        .grid-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        .info-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            backdrop-filter: blur(10px);
        }
        .chart-container {
            height: 300px;
            margin-top: 20px;
        }
        .key-point {
            margin-bottom: 15px;
            display: flex;
            align-items: start;
            gap: 10px;
        }
        .icon {
            color: #4CAF50;
            margin-top: 4px;
        }
    </style>
</head>
<body>
    <div class="slide">
        <h1 class="title">Ситуация на рынке Forex в 2025 году</h1>
        
        <div class="grid-container">
            <div class="info-card">
                <div class="key-point">
                    <i class="fas fa-chart-line icon"></i>
                    <div>
                        <strong>Мировая экономика:</strong> Умеренный рост 3.3%, влияние на движение валют через экономические показатели
                    </div>
                </div>
                <div class="key-point">
                    <i class="fas fa-university icon"></i>
                    <div>
                        <strong>Монетарная политика:</strong> Активное управление ставками центральными банками для контроля инфляции
                    </div>
                </div>
                <div class="key-point">
                    <i class="fas fa-globe icon"></i>
                    <div>
                        <strong>Геополитические факторы:</strong> Торговые войны, региональные конфликты влияют на валютные курсы
                    </div>
                </div>
                <div class="key-point">
                    <i class="fas fa-vote-yea icon"></i>
                    <div>
                        <strong>Влияние выборов в США:</strong> Значительное влияние на USD и связанные пары
                    </div>
                </div>
            </div>
            
            <div class="info-card">
                <h3 class="text-xl font-bold mb-4">Волатильность основных валютных пар</h3>
                <div class="chart-container">
                    <canvas id="volatilityChart"></canvas>
                </div>
            </div>
        </div>
    </div>

    <script>
        const ctx = document.getElementById('volatilityChart').getContext('2d');
        new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['2022', '2023', '2024', '2025'],
                datasets: [{
                    label: 'Средняя волатильность (%)',
                    data: [10.6, 9.0, 7.3, 6.8],
                    borderColor: '#4CAF50',
                    backgroundColor: 'rgba(76, 175, 80, 0.1)',
                    fill: true,
                    tension: 0.4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        labels: {
                            color: 'white'
                        }
                    }
                },
                scales: {
                    y: {
                        ticks: {
                            color: 'white'
                        },
                        grid: {
                            color: 'rgba(255, 255, 255, 0.1)'
                        }
                    },
                    x: {
                        ticks: {
                            color: 'white'
                        },
                        grid: {
                            color: 'rgba(255, 255, 255, 0.1)'
                        }
                    }
                }
            }
        });
    </script>
</body>
</html>
2 / 7
Preview
Code
Fact check content
Select to edit
Copy<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            font-family: 'Roboto', sans-serif;
            color: white;
        }
        .slide {
            width: 1280px;
            min-height: 720px;
            margin: 0 auto;
            padding: 40px;
        }
        .title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
        }
        .table-container {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 30px;
            backdrop-filter: blur(10px);
        }
        table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
        }
        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        th {
            background: rgba(255, 255, 255, 0.1);
            font-weight: 500;
        }
        .stats-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }
        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
        }
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #4CAF50;
            margin-bottom: 10px;
        }
        .stat-description {
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.9);
        }
    </style>
</head>
<body>
    <div class="slide">
        <h1 class="title">Требования ведущих проп-фирм</h1>
        
        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th>Проп-фирма</th>
                        <th>Challenge прибыль</th>
                        <th>Verification прибыль</th>
                        <th>Макс. просадка</th>
                        <th>Дневная просадка</th>
                        <th>Разделение прибыли</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>FTMO</td>
                        <td>10%</td>
                        <td>5%</td>
                        <td>10%</td>
                        <td>5%</td>
                        <td>До 90%</td>
                    </tr>
                    <tr>
                        <td>The5ers</td>
                        <td>10%</td>
                        <td>-</td>
                        <td>6%</td>
                        <td>3%</td>
                        <td>До 100%</td>
                    </tr>
                    <tr>
                        <td>E8 Markets</td>
                        <td>5%</td>
                        <td>5%</td>
                        <td>5%</td>
                        <td>-</td>
                        <td>80-100%</td>
                    </tr>
                    <tr>
                        <td>Fidelcrest</td>
                        <td>10-15%</td>
                        <td>Удвоенные</td>
                        <td>Варьируется</td>
                        <td>Варьируется</td>
                        <td>80-90%</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="stats-container">
            <div class="stat-card">
                <div class="stat-number">1-2%</div>
                <div class="stat-description">Клиентов получают регулярные выплаты</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">7%</div>
                <div class="stat-description">Счетов получили выплаты в 2024 году из 300,000</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">4%</div>
                <div class="stat-description">Средняя выплата от размера финансируемого плана</div>
            </div>
        </div>
    </div>
</body>
</html>
3 / 7
Preview
Code
Fact check content
Select to edit
Copy<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            font-family: 'Roboto', sans-serif;
            color: white;
        }
        .slide {
            width: 1280px;
            min-height: 720px;
            margin: 0 auto;
            padding: 40px;
        }
        .title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
        }
        .grid-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        .table-container {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            backdrop-filter: blur(10px);
        }
        table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
        }
        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        th {
            background: rgba(255, 255, 255, 0.1);
            font-weight: 500;
        }
        .correlation-container {
            height: 300px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="slide">
        <h1 class="title">Популярные валютные пары и их характеристики</h1>
        
        <div class="grid-container">
            <div class="table-container">
                <table>
                    <thead>
                        <tr>
                            <th>Валютная пара</th>
                            <th>Дневная волатильность</th>
                            <th>Спред</th>
                            <th>Активные сессии</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>EUR/USD</td>
                            <td>80-112 пипс (5.92%)</td>
                            <td>0.0-1.7</td>
                            <td>Лондон, Нью-Йорк</td>
                        </tr>
                        <tr>
                            <td>GBP/USD</td>
                            <td>80-150 пипс (6.33%)</td>
                            <td>0.0-1.6</td>
                            <td>Лондон, Нью-Йорк</td>
                        </tr>
                        <tr>
                            <td>USD/JPY</td>
                            <td>70-160 пипс (13.27%)</td>
                            <td>0.7-1.6</td>
                            <td>Токио, Лондон</td>
                        </tr>
                        <tr>
                            <td>AUD/USD</td>
                            <td>70-100 пипс</td>
                            <td>0.0-1.5</td>
                            <td>Сидней, Токио</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            
            <div class="table-container">
                <h3 class="text-xl font-bold mb-4">Корреляция валютных пар</h3>
                <div class="correlation-container">
                    <canvas id="correlationChart"></canvas>
                </div>
            </div>
        </div>
    </div>

    <script>
        const ctx = document.getElementById('correlationChart').getContext('2d');
        new Chart(ctx, {
            type: 'heatmap',
            data: {
                labels: ['EUR/USD', 'GBP/USD', 'USD/JPY', 'AUD/USD'],
                datasets: [{
                    label: 'EUR/USD',
                    data: [1, 0.89, -0.95, 0.65],
                    backgroundColor: '#4CAF50'
                },
                {
                    label: 'GBP/USD',
                    data: [0.89, 1, -0.85, 0.72],
                    backgroundColor: '#2196F3'
                },
                {
                    label: 'USD/JPY',
                    data: [-0.95, -0.85, 1, -0.58],
                    backgroundColor: '#F44336'
                },
                {
                    label: 'AUD/USD',
                    data: [0.65, 0.72, -0.58, 1],
                    backgroundColor: '#FFC107'
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        display: true,
                        position: 'top',
                        labels: {
                            color: 'white'
                        }
                    }
                },
                scales: {
                    y: {
                        ticks: {
                            color: 'white'
                        },
                        grid: {
                            color: 'rgba(255, 255, 255, 0.1)'
                        }
                    },
                    x: {
                        ticks: {
                            color: 'white'
                        },
                        grid: {
                            color: 'rgba(255, 255, 255, 0.1)'
                        }
                    }
                }
            }
        });
    </script>
</body>
</html>
4 / 7
Preview
Code
Fact check content
Select to edit
Copy<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/mermaid@11.6.0/dist/mermaid.min.js"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            font-family: 'Roboto', sans-serif;
            color: white;
        }
        .slide {
            width: 1280px;
            min-height: 720px;
            margin: 0 auto;
            padding: 40px;
        }
        .title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
        }
        .stages-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-bottom: 30px;
        }
        .stage-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            backdrop-filter: blur(10px);
        }
        .stage-title {
            font-size: 1.5rem;
            font-weight: 500;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .stage-icon {
            color: #4CAF50;
        }
        .action-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        .action-item {
            margin-bottom: 10px;
            display: flex;
            align-items: start;
            gap: 8px;
        }
        .action-icon {
            color: #4CAF50;
            margin-top: 4px;
        }
        .warning-section {
            background: rgba(244, 67, 54, 0.1);
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
        }
        .warning-title {
            font-size: 1.2rem;
            font-weight: 500;
            margin-bottom: 10px;
            color: #F44336;
            display: flex;
            align-items: center;
            gap: 8px;
        }
    </style>
</head>
<body>
    <div class="slide">
        <h1 class="title">План действий на каждом этапе проп-программы</h1>
        
        <div class="stages-container">
            <div class="stage-card">
                <div class="stage-title">
                    <i class="fas fa-flag-checkered stage-icon"></i>
                    Challenge этап
                </div>
                <ul class="action-list">
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Разработка детального торгового плана</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Тестирование стратегии на демо-счете</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Строгое управление рисками (1-2% на сделку)</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Ведение подробного трейд-журнала</span>
                    </li>
                </ul>
            </div>

            <div class="stage-card">
                <div class="stage-title">
                    <i class="fas fa-shield-alt stage-icon"></i>
                    Verification этап
                </div>
                <ul class="action-list">
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Следование проверенной стратегии</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Контроль эмоций и дисциплина</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Соблюдение правил проп-фирмы</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Анализ результатов и корректировки</span>
                    </li>
                </ul>
            </div>

            <div class="stage-card">
                <div class="stage-title">
                    <i class="fas fa-crown stage-icon"></i>
                    Funded этап
                </div>
                <ul class="action-list">
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Ответственное управление капиталом</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Постепенное масштабирование</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Регулярная отчетность</span>
                    </li>
                    <li class="action-item">
                        <i class="fas fa-check action-icon"></i>
                        <span>Непрерывное обучение и развитие</span>
                    </li>
                </ul>
            </div>
        </div>

        <div class="warning-section">
            <div class="warning-title">
                <i class="fas fa-exclamation-triangle"></i>
                Типичные ошибки, которых следует избегать
            </div>
            <ul class="action-list">
                <li class="action-item">
                    <i class="fas fa-times" style="color: #F44336;"></i>
                    <span>Чрезмерная торговля и погоня за прибылью</span>
                </li>
                <li class="action-item">
                    <i class="fas fa-times" style="color: #F44336;"></i>
                    <span>Игнорирование правил управления рисками</span>
                </li>
                <li class="action-item">
                    <i class="fas fa-times" style="color: #F44336;"></i>
                    <span>Торговля под влиянием эмоций</span>
                </li>
                <li class="action-item">
                    <i class="fas fa-times" style="color: #F44336;"></i>
                    <span>Использование чрезмерного кредитного плеча</span>
                </li>
            </ul>
        </div>
    </div>
</body>
</html>
5 / 7
Preview
Code
Fact check content
Select to edit
Copy<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            font-family: 'Roboto', sans-serif;
            color: white;
        }
        .slide {
            width: 1280px;
            min-height: 720px;
            margin: 0 auto;
            padding: 40px;
        }
        .title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
        }
        .strategies-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 30px;
        }
        .strategy-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            backdrop-filter: blur(10px);
        }
        .strategy-title {
            font-size: 1.3rem;
            font-weight: 500;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #4CAF50;
        }
        .strategy-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        .strategy-item {
            margin-bottom: 10px;
            display: flex;
            align-items: start;
            gap: 8px;
        }
        .management-container {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
        }
        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            margin-top: 15px;
        }
        .metric-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            padding: 15px;
            text-align: center;
        }
        .metric-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: #4CAF50;
            margin-bottom: 5px;
        }
        .metric-label {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.9);
        }
    </style>
</head>
<body>
    <div class="slide">
        <h1 class="title">Эффективные стратегии и манименеджмент</h1>
        
        <div class="strategies-container">
            <div class="strategy-card">
                <div class="strategy-title">
                    <i class="fas fa-chart-line"></i>
                    Трендовый рынок
                </div>
                <ul class="strategy-list">
                    <li class="strategy-item">
                        <i class="fas fa-play-circle"></i>
                        <span>Breakout (пробой уровней)</span>
                    </li>
                    <li class="strategy-item">
                        <i class="fas fa-reply"></i>
                        <span>Pullback (откат к уровням)</span>
                    </li>
                    <li class="strategy-item">
                        <i class="fas fa-layer-group"></i>
                        <span>Pyramiding (наращивание)</span>
                    </li>
                </ul>
            </div>

            <div class="strategy-card">
                <div class="strategy-title">
                    <i class="fas fa-exchange-alt"></i>
                    Флэтовый рынок
                </div>
                <ul class="strategy-list">
                    <li class="strategy-item">
                        <i class="fas fa-compress-arrows-alt"></i>
                        <span>Range-bound торговля</span>
                    </li>
                    <li class="strategy-item">
                        <i class="fas fa-sync-alt"></i>
                        <span>Mean-reversion</span>
                    </li>
                    <li class="strategy-item">
                        <i class="fas fa-bolt"></i>
                        <span>Скальпинг</span>
                    </li>
                </ul>
            </div>

            <div class="strategy-card">
                <div class="strategy-title">
                    <i class="fas fa-newspaper"></i>
                    Торговля на новостях
                </div>
                <ul class="strategy-list">
                    <li class="strategy-item">
                        <i class="fas fa-door-open"></i>
                        <span>Пробой после новостей</span>
                    </li>
                    <li class="strategy-item">
                        <i class="fas fa-random"></i>
                        <span>Контр-тренд на реакции</span>
                    </li>
                    <li class="strategy-item">
                        <i class="fas fa-arrows-alt-h"></i>
                        <span>Стрэддл стратегии</span>
                    </li>
                </ul>
            </div>
        </div>

        <div class="management-container">
            <h2 class="text-xl font-bold mb-3">Ключевые метрики манименеджмента</h2>
            <div class="metrics-grid">
                <div class="metric-card">
                    <div class="metric-value">1:2+</div>
                    <div class="metric-label">Минимальное соотношение риск/прибыль</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value">1-2%</div>
                    <div class="metric-label">Риск на сделку от баланса</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value">5%</div>
                    <div class="metric-label">Максимальный дневной лимит потерь</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value">10%</div>
                    <div class="metric-label">Максимальный недельный лимит потерь</div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
6 / 7
Preview
Code
Fact check content
Select to edit
Copy<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            font-family: 'Roboto', sans-serif;
            color: white;
        }
        .slide {
            width: 1280px;
            min-height: 720px;
            margin: 0 auto;
            padding: 40px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
        }
        .success-factors {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-bottom: 40px;
            width: 100%;
        }
        .factor-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            backdrop-filter: blur(10px);
            text-align: center;
            transition: transform 0.3s ease;
        }
        .factor-card:hover {
            transform: translateY(-5px);
        }
        .factor-icon {
            font-size: 2.5rem;
            color: #4CAF50;
            margin-bottom: 15px;
        }
        .factor-title {
            font-size: 1.2rem;
            font-weight: 500;
            margin-bottom: 10px;
            color: #4CAF50;
        }
        .factor-description {
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.9);
            line-height: 1.5;
        }
        .quote-container {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 30px;
            margin-top: 20px;
            text-align: center;
            max-width: 800px;
            position: relative;
        }
        .quote-icon {
            font-size: 2rem;
            color: #4CAF50;
            margin-bottom: 15px;
        }
        .quote-text {
            font-size: 1.3rem;
            font-style: italic;
            margin-bottom: 15px;
            line-height: 1.6;
        }
        .quote-author {
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.8);
        }
    </style>
</head>
<body>
    <div class="slide">
        <h1 class="title">Ключевые факторы успеха в проп-трейдинге</h1>
        
        <div class="success-factors">
            <div class="factor-card">
                <i class="fas fa-brain factor-icon"></i>
                <div class="factor-title">Психологическая устойчивость</div>
                <div class="factor-description">
                    Контроль эмоций, дисциплина и способность придерживаться торгового плана даже в стрессовых ситуациях
                </div>
            </div>

            <div class="factor-card">
                <i class="fas fa-shield-alt factor-icon"></i>
                <div class="factor-title">Управление рисками</div>
                <div class="factor-description">
                    Строгое соблюдение правил риск-менеджмента и защита капитала как главный приоритет
                </div>
            </div>

            <div class="factor-card">
                <i class="fas fa-chart-bar factor-icon"></i>
                <div class="factor-title">Проверенная стратегия</div>
                <div class="factor-description">
                    Последовательное применение тестированной и оптимизированной торговой системы
                </div>
            </div>
        </div>

        <div class="success-factors">
            <div class="factor-card">
                <i class="fas fa-sync factor-icon"></i>
                <div class="factor-title">Адаптивность</div>
                <div class="factor-description">
                    Способность приспосабливаться к меняющимся рыночным условиям и корректировать стратегию
                </div>
            </div>

            <div class="factor-card">
                <i class="fas fa-graduation-cap factor-icon"></i>
                <div class="factor-title">Постоянное обучение</div>
                <div class="factor-description">
                    Непрерывное развитие навыков и изучение новых торговых подходов
                </div>
            </div>

            <div class="factor-card">
                <i class="fas fa-clipboard-check factor-icon"></i>
                <div class="factor-title">Анализ результатов</div>
                <div class="factor-description">
                    Регулярный анализ сделок и корректировка действий на основе полученного опыта
                </div>
            </div>
        </div>

        <div class="quote-container">
            <i class="fas fa-quote-right quote-icon"></i>
            <div class="quote-text">
                "Успех в трейдинге приходит к тем, кто сочетает терпение мудреца с дисциплиной воина"
            </div>
            <div class="quote-author">
                — Правило успешного проп-трейдера
            </div>
        </div>
    </div>
</body>
</html>