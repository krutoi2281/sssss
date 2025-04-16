<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jony.edu - ЕНТ дайындық</title>
    <style>
         *{
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        .body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            background-color: #f5f7fa;
            color: #333;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        header {
            background: linear-gradient(135deg, #4CAF50, #2196F3);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            cursor: pointer;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-weight: 500;
            transition: opacity 0.3s;
        }
        
        nav a:hover {
            opacity: 0.8;
        }
        
        .hero {
            text-align: center;
            padding: 4rem 0;
            background: linear-gradient(rgba(255,255,255,0.9), rgba(255,255,255,0.9)), 
                        url('https://via.placeholder.com/1200x400') center/cover;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #2c3e50;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: #7f8c8d;
        }
        
        .btn {
            display: inline-block;
            background: #4CAF50;
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }
        
        .btn:hover {
            background: #3e8e41;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        .section {
            padding: 3rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 2rem;
            font-size: 2rem;
            color: #2c3e50;
        }
        .subjects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 2rem;
        }
        
        .subject-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            cursor: pointer;
        }
        
        .subject-card:hover {
            transform: translateY(-10px);
        }
        
        .subject-img {
            height: 150px;
            background: #ddd;
            background-size: cover;
            background-position: center;
        }
        
        .subject-info {
            padding: 20px;
        }
        
        .subject-info h3 {
            margin-bottom: 10px;
            color: #2c3e50;
        }
        
        .subject-info p {
            color: #7f8c8d;
            margin-bottom: 15px;
        }
        .test-container {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            max-width: 800px;
            margin: 2rem auto;
            display: none;
        }
        
        .test-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
        }
        
        .timer {
            font-size: 1.2rem;
            font-weight: bold;
            color: #e74c3c;
        }
        
        .question {
            margin-bottom: 2rem;
        }
        
        .question-text {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            font-weight: 500;
        }
        
        .option {
            display: block;
            margin-bottom: 10px;
            padding: 10px 15px;
            background: #f8f9fa;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .option:hover {
            background: #e9ecef;
        }
        
        .option input {
            margin-right: 10px;
        }
        
        .test-nav {
            display: flex;
            justify-content: space-between;
            margin-top: 2rem;
        }
        .results-container {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            max-width: 800px;
            margin: 2rem auto;
            display: none;
        }
        
        .results-title {
            text-align: center;
            margin-bottom: 2rem;
            color: #2c3e50;
        }
        
        .score {
            font-size: 2rem;
            text-align: center;
            margin: 2rem 0;
            color: #4CAF50;
        }
        
        .mistakes-list {
            margin-top: 2rem;
        }
        
        .mistake {
            background: #fff8e1;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
        }
        
        .mistake-question {
            font-weight: 500;
            margin-bottom: 5px;
        }
        
        .correct-answer {
            color: #4CAF50;
            font-weight: bold;
        }
    
        .stats-container {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            margin-top: 2rem;
            display: none;
        }
        
        .progress-bar {
            height: 20px;
            background: #f1f1f1;
            border-radius: 10px;
            margin-bottom: 1rem;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background: #4CAF50;
            width: 0%;
            transition: width 1s;
        }
        
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 3rem;
        }
        

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
            }
            
            nav {
                margin-top: 1rem;
            }
            
            nav a {
                margin: 0 10px;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container header-content">
            <div class="logo" onclick="showHome()">Jony.edu</div>
            <nav>
                <a href="#" onclick="showHome()">Басты бет</a>
                <a href="#" onclick="showSubjects()">Пәндер</a>
                <a href="#" onclick="showStats()">Статистика</a>
                <a href="#" onclick="startENTTest()">ЕНТ Тест</a>
            </nav>
        </div>
    </header>


    <section class="hero">
        <div class="container">
            <h1>Jony.edu - Сынық білім платформасы</h1>
            <p>Убт дайындық</p>
            <button class="btn" onclick="startENTTest()">Тестті бастау</button>
        </div>
    </section>


    <div class="container">

        <div id="home-page">
            <section class="section">
                <h2 class="section-title">Неге Jony.edu таңдау керек?</h2>
                <div class="subjects-grid">
                    <div class="subject-card">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>ЕНТ тесттері</h3>
                            <p>Нақты ЕНТ сынағына ұқсас тесттер</p>
                        </div>
                    </div>
                    <div class="subject-card">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Қателерді талдау</h3>
                            <p>Әрбір тесттен кейін егжей-тегжейлі түсіндіру</p>
                        </div>
                    </div>
                    <div class="subject-card">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Бейімделген оқыту</h3>
                            <p>Сіздің білім деңгейіңізге сай сұрақтар</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>


        <div id="subjects-page" style="display: none;">
            <section class="section">
                <h2 class="section-title">Пәнді таңдаңыз</h2>
                <div class="subjects-grid">
                    <div class="subject-card" onclick="startSubjectTest('math')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Математика</h3>
                            <p>Алгебра, геометрия және математикалық талдау</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('history')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Қазақстан тарихы</h3>
                            <p>Ежелгі заманнан бүгінгі күнге дейін</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('kazakh')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Қазақ тілі</h3>
                            <p>Грамматика, лексика және әдебиет</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('russian')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Орыс тілі</h3>
                            <p>Грамматика және тесттер</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('physics')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Физика</h3>
                            <p>Механика, термодинамика және электродинамика</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                    <div class="subject-card" onclick="startSubjectTest('chemistry')">
                        <div class="subject-img" style="background-image: url('https://via.placeholder.com/300x200');"></div>
                        <div class="subject-info">
                            <h3>Химия</h3>
                            <p>Органикалық және бейорганикалық химия</p>
                            <button class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Тестті бастау</button>
                        </div>
                    </div>
                </div>
            </section>
        </div>


        <div id="ent-test-page" class="test-container">
            <div class="test-header">
                <h2>ЕНТ Тесті</h2>
                <div class="timer" id="timer">20:00</div>
            </div>
            
            <div id="question-container">

            </div>
            
            <div class="test-nav">
                <button class="btn" id="prev-btn" onclick="prevQuestion()" disabled>Артқа</button>
                <button class="btn" id="next-btn" onclick="nextQuestion()">Келесі</button>
                <button class="btn" id="finish-btn" onclick="finishTest()" style="display: none;">Тестті аяқтау</button>
            </div>
        </div>
        <div id="results-page" class="results-container">
            <h2 class="results-title">Тест нәтижелері</h2>
            <div class="score" id="score">Сіздің нәтижеңіз: 0/20</div>
            
            <div class="progress-bar">
                <div class="progress" id="progress-bar"></div>
            </div>
            
            <h3>Қателерді талдау:</h3>
            <div class="mistakes-list" id="mistakes-list">
            </div>
            
            <button class="btn" onclick="showHome()" style="margin-top: 2rem;">Басты бетке оралу</button>
        </div>
        <div id="stats-page" class="stats-container">
            <h2 class="section-title">Сіздің статистикаңыз</h2>
            
            <h3>Пәндер бойынша прогресс:</h3>
            <div style="margin: 1rem 0;">
                <p>Математика</p>
                <div class="progress-bar">
                    <div class="progress" style="width: 65%;"></div>
                </div>
            </div>
            
            <div style="margin: 1rem 0;">
                <p>Қазақстан тарихы</p>
                <div class="progress-bar">
                    <div class="progress" style="width: 45%;"></div>
                </div>
            </div>
            
            <div style="margin: 1rem 0;">
                <p>Қазақ тілі</p>
                <div class="progress-bar">
                    <div class="progress" style="width: 30%;"></div>
                </div>
            </div>
            
            <h3 style="margin-top: 2rem;">Соңғы нәтижелер:</h3>
            <ul id="last-results" style="margin: 1rem 0; list-style: none;">
                <li>ЕНТ Тесті: 15/20 (75%)</li>
                <li>Математика: 8/10 (80%)</li>
                <li>Тарих: 6/10 (60%)</li>
            </ul>
            
            <button class="btn" onclick="showHome()" style="margin-top: 1rem;">Басты бетке оралу</button>
        </div>
    </div>


    <footer>
        <div class="container">
            <p>© 2024 Jony.edu - Барлық құқықтар қорғалған</p>
            <p>Бірыңғай ұлттық тестілеуге дайындық</p>
        </div>
    </footer>

    <script>

        const appState = {
            currentPage: 'home',
            currentTest: null,
            currentQuestion: 0,
            answers: [],
            timer: null,
            timeLeft: 1200
        };

  
        const testDatabase = {
            ent: [
                {
                    question: "Қай сан жай сан болып табылады?",
                    options: ["4", "7", "9", "12"],
                    correct: 1,
                    subject: "math"
                },
                {
                    question: "Қазақстан қай жылы тәуелсіздік алды?",
                    options: ["1989", "1990", "1991", "1992"],
                    correct: 2,
                    subject: "history"
                },
                {
                    question: "Қазақстанның астанасы - бұл:",
                    options: ["Алматы", "Шымкент", "Нұр-Сұлтан", "Қарағанды"],
                    correct: 2,
                    subject: "history"
                },
                {
                    question: "2 + 2 × 2 = ?",
                    options: ["6", "8", "4", "10"],
                    correct: 0,
                    subject: "math"
                },
                {
                    question: "Қазақ хандығының алғашқы ханы кім?",
                    options: ["Абылай хан", "Керей хан", "Жәнібек хан", "Қасым хан"],
                    correct: 2,
                    subject: "history"
                },
                {
                    question: "π (пи) санының мәні қандай?",
                    options: ["3.12", "3.14", "3.16", "3.18"],
                    correct: 1,
                    subject: "math"
                },
                {
                    question: "Қазақ тіліндегі септіктер саны қанша?",
                    options: ["5", "6", "7", "8"],
                    correct: 2,
                    subject: "kazakh"
                },
                {
                    question: "Алматы қаласы қай жылы құрылды?",
                    options: ["1854", "1867", "1883", "1895"],
                    correct: 0,
                    subject: "history"
                },
                {
                    question: "Сутегінің химиялық белгісі қандай?",
                    options: ["H", "He", "O", "N"],
                    correct: 0,
                    subject: "chemistry"
                },
                {
                    question: "Қазақстанның ең биік тауы қайсы?",
                    options: ["Хан Тәңірі", "Белуха", "Жеңіс", "Талғар"],
                    correct: 1,
                    subject: "geography"
                },
                {
                    question: "Тәуелсіз Қазақстанның алғашқы Конституциясы қабылданған жыл?",
                    options: ["1991", "1993", "1995", "1997"],
                    correct: 2,
                    subject: "history"
                },
                {
                    question: "Фотосинтез процесі қай органеллада жүреді?",
                    options: ["Митохондрия", "Хлоропласт", "Ядро", "Рибосома"],
                    correct: 1,
                    subject: "biology"
                },
                {
                    question: "Қазақстандағы ең ұзын өзен қайсы?",
                    options: ["Ертіс", "Сырдария", "Іле", "Жайық"],
                    correct: 0,
                    subject: "geography"
                },
                {
                    question: "Қазақ әліпбиіндегі әріптер саны қанша?",
                    options: ["28", "33", "42", "38"],
                    correct: 2,
                    subject: "kazakh"
                },
                {
                    question: "Ньютонның екінші заңы қандай формуламен өрнектеледі?",
                    options: ["F=ma", "E=mc²", "P=IV", "V=IR"],
                    correct: 0,
                    subject: "physics"
                },
                {
                    question: "Қазақстанның ұлттық валютасы қашан енгізілді?",
                    options: ["1991", "1993", "1995", "1997"],
                    correct: 1,
                    subject: "history"
                },
                {
                    question: "Температураны өлшейтін құрал?",
                    options: ["Барометр", "Термометр", "Анемометр", "Гигрометр"],
                    correct: 1,
                    subject: "physics"
                },
                {
                    question: "Қазақстанның халқы қанша миллион адам? (2023 ж.)",
                    options: ["15", "18", "20", "22"],
                    correct: 2,
                    subject: "geography"
                },
                {
                    question: "Қазақстандағы ең үлкен көл қайсы?",
                    options: ["Балқаш", "Зайсан", "Алакөл", "Каспий"],
                    correct: 3,
                    subject: "geography"
                },
                {
                    question: "Қазақ тіліндегі етістік категориялары қанша?",
                    options: ["3", "5", "7", "9"],
                    correct: 2,
                    subject: "kazakh"
                },
                {
                    question: "Қуаңшылыққа төзімді өсімдік?",
                    options: ["Қызғалдақ", "Кактус", "Раушан", "Қалампыр"],
                    correct: 1,
                    subject: "biology"
                },
                {
                    question: "Қазақстанның ең ірі қаласы (халық саны бойынша)?",
                    options: ["Алматы", "Нұр-Сұлтан", "Шымкент", "Қарағанды"],
                    correct: 0,
                    subject: "geography"
                },
                {
                    question: "Қазақстан Конституциясы қашан қабылданды?",
                    options: ["1991", "1993", "1995", "1997"],
                    correct: 2,
                    subject: "history"
                },
                {
                    question: "Қышқылды анықтау үшін қандай индикатор қолданылады?",
                    options: ["Фенолфталеин", "Лакмус", "Метилоранж", "Бромтимол көк"],
                    correct: 1,
                    subject: "chemistry"
                },
                {
                    question: "Қазақстанның ұлттық символдары қанша?",
                    options: ["3", "5", "7", "9"],
                    correct: 2,
                    subject: "history"
                },
                {
                    question: "Қазақ тіліндегі сөз таптары қанша?",
                    options: ["5", "7", "9", "11"],
                    correct: 2,
                    subject: "kazakh"
                },
                {
                    question: "Қазақстандағы ең ұзын темір жол қайсы?",
                    options: ["Транс-Каспий", "Туркістан-Сібір", "Орталық-Азия", "Оңтүстік-Солтүстік"],
                    correct: 1,
                    subject: "geography"
                },
                {
                    question: "Қазақстанның ұлттық аспабы?",
                    options: ["Домбыра", "Қобыз", "Сыбызғы", "Жетіген"],
                    correct: 0,
                    subject: "culture"
                },
                {
                    question: "Қазақстандағы ең ірі университет қайсы?",
                    options: ["ҚазҰУ", "Әл-Фараби атындағы ҚазҰУ", "Еуразия ұлттық университеті", "Сәтбаев университеті"],
                    correct: 1,
                    subject: "education"
                },
                {
                    question: "Қазақстанның ұлттық валютасы?",
                    options: ["Теңге", "Сом", "Рубль", "Доллар"],
                    correct: 0,
                    subject: "economics"
                },
                {
                    question: "Қазақстанның ұлттық биі?",
                    options: ["Қара жорға", "Ортеке", "Қыз Жібек", "Айжан қыз"],
                    correct: 0,
                    subject: "culture"
                }
            ],
            math: [
                {
                    question: "x² - 4 = 0 теңдеуінің шешімі қандай?",
                    options: ["-2", "2", "-2 және 2", "Шешімі жоқ"],
                    correct: 2,
                    subject: "math"
                },
                {
                    question: "π (пи) санының мәні қандай?",
                    options: ["3.12", "3.14", "3.16", "3.18"],
                    correct: 1,
                    subject: "math"
                },
                {
                    question: "Тік төртбұрыштың ауданы қалай есептеледі?",
                    options: ["Қабырғаларын қосу", "Ұзындығын биіктікке көбейту", "Периметрін есептеу", "Диагональды табу"],
                    correct: 1,
                    subject: "math"
                }
            ],
            history: [
                {
                    question: "Қазақ хандығының алғашқы ханы кім?",
                    options: ["Абылай хан", "Керей хан", "Жәнібек хан", "Қасым хан"],
                    correct: 2,
                    subject: "history"
                },
                {
                    question: "Алматы қаласы қай жылы құрылды?",
                    options: ["1854", "1867", "1883", "1895"],
                    correct: 0,
                    subject: "history"
                },
                {
                    question: "Тәуелсіз Қазақстанның алғашқы Конституциясы қабылданған жыл?",
                    options: ["1991", "1993", "1995", "1997"],
                    correct: 2,
                    subject: "history"
                }
            ]
        };


        function showHome() {
            document.getElementById('home-page').style.display = 'block';
            document.getElementById('subjects-page').style.display = 'none';
            document.getElementById('ent-test-page').style.display = 'none';
            document.getElementById('results-page').style.display = 'none';
            document.getElementById('stats-page').style.display = 'none';
            appState.currentPage = 'home';
        }


        function showSubjects() {
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('subjects-page').style.display = 'block';
            document.getElementById('ent-test-page').style.display = 'none';
            document.getElementById('results-page').style.display = 'none';
            document.getElementById('stats-page').style.display = 'none';
            appState.currentPage = 'subjects';
        }


        function showStats() {
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('subjects-page').style.display = 'none';
            document.getElementById('ent-test-page').style.display = 'none';
            document.getElementById('results-page').style.display = 'none';
            document.getElementById('stats-page').style.display = 'block';
            appState.currentPage = 'stats';
        }


        function startENTTest() {
            appState.currentTest = 'ent';
            appState.currentQuestion = 0;
            appState.answers = new Array(testDatabase.ent.length).fill(null);
            
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('subjects-page').style.display = 'none';
            document.getElementById('ent-test-page').style.display = 'block';
            document.getElementById('results-page').style.display = 'none';
            document.getElementById('stats-page').style.display = 'none';
            
            startTimer();
            showQuestion();
        }

        function startSubjectTest(subject) {
            appState.currentTest = subject;
            appState.currentQuestion = 0;
            appState.answers = new Array(testDatabase[subject].length).fill(null);
            
            document.getElementById('home-page').style.display = 'none';
            document.getElementById('subjects-page').style.display = 'none';
            document.getElementById('ent-test-page').style.display = 'block';
            document.getElementById('results-page').style.display = 'none';
            document.getElementById('stats-page').style.display = 'none';
            

            document.getElementById('timer').style.display = 'none';
            showQuestion();
        }

   
        function showQuestion() {
            const container = document.getElementById('question-container');
            const test = testDatabase[appState.currentTest];
            const question = test[appState.currentQuestion];
            
            container.innerHTML = `
                <div class="question">
                    <p class="question-text">${appState.currentQuestion + 1}. ${question.question}</p>
                    ${question.options.map((option, index) => `
                        <label class="option">
                            <input type="radio" name="answer" value="${index}" 
                                   ${appState.answers[appState.currentQuestion] === index ? 'checked' : ''}>
                            ${option}
                        </label>
                    `).join('')}
                </div>
            `;
            

            document.getElementById('prev-btn').disabled = appState.currentQuestion === 0;
            
            if (appState.currentQuestion === test.length - 1) {
                document.getElementById('next-btn').style.display = 'none';
                document.getElementById('finish-btn').style.display = 'inline-block';
            } else {
                document.getElementById('next-btn').style.display = 'inline-block';
                document.getElementById('finish-btn').style.display = 'none';
            }
        }

   
        function nextQuestion() {
            saveAnswer();
            appState.currentQuestion++;
            showQuestion();
        }

      
        function prevQuestion() {
            saveAnswer();
            appState.currentQuestion--;
            showQuestion();
        }

 
        function saveAnswer() {
            const selected = document.querySelector('input[name="answer"]:checked');
            if (selected) {
                appState.answers[appState.currentQuestion] = parseInt(selected.value);
            }
        }

    
        function finishTest() {
            saveAnswer();
            clearInterval(appState.timer);
            
  
            const test = testDatabase[appState.currentTest];
            let correct = 0;
            const mistakes = [];
            
            for (let i = 0; i < test.length; i++) {
                if (appState.answers[i] === test[i].correct) {
                    correct++;
                } else {
                    mistakes.push({
                        question: test[i].question,
                        correctAnswer: test[i].options[test[i].correct],
                        userAnswer: appState.answers[i] !== null ? test[i].options[appState.answers[i]] : "Жауап жоқ"
                    });
                }
            }
            document.getElementById('ent-test-page').style.display = 'none';
            document.getElementById('results-page').style.display = 'block';
            
            const score = document.getElementById('score');
            score.textContent = `Сіздің нәтижеңіз: ${correct}/${test.length}`;
            
            const progress = document.getElementById('progress-bar');
            progress.style.width = `${(correct / test.length) * 100}%`;
            
            const mistakesList = document.getElementById('mistakes-list');
            mistakesList.innerHTML = mistakes.map(mistake => `
                <div class="mistake">
                    <p class="mistake-question">${mistake.question}</p>
                    <p>Сіздің жауабыңыз: ${mistake.userAnswer}</p>
                    <p class="correct-answer">Дұрыс жауап: ${mistake.correctAnswer}</p>
                </div>
            `).join('');
        }


        function startTimer() {
            appState.timeLeft = 1200;
            updateTimerDisplay();
            
            appState.timer = setInterval(() => {
                appState.timeLeft--;
                updateTimerDisplay();
                
                if (appState.timeLeft <= 0) {
                    clearInterval(appState.timer);
                    finishTest();
                }
            }, 1000);
        }

        function updateTimerDisplay() {
            const minutes = Math.floor(appState.timeLeft / 60);
            const seconds = appState.timeLeft % 60;
            document.getElementById('timer').textContent = 
                `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }
        showHome();
    </script>
</body>
</html>
