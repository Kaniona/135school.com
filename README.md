<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>№ 135 А.Тоқмағанбетов атындағы орта мектеп <img src="135.jpg" alt="Мектеп суреті"></title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: #f0f4f7;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
            transition: background-color 1s ease;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        .photo-container {
        display: flex;
        justify-content: space-between;
        padding: 30px;
        }

        .photo-left {
        order: 1; 
        max-width: 45%; 
        }

        .photo-right {
        order: 1; 
        max-width: 45%; 
        }

        header {
            background-image: url('135.jpg');
            background-size: cover;
            color: white;
            text-align: center;
            padding: 100px 20px;
            position: relative;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            animation: headerAnimation 1s ease-out;
        }

        @keyframes headerAnimation {
            0% {
                opacity: 0;
                transform: translateY(-50px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        header h1 {
            font-size: 4em;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 5px;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.5em;
            text-transform: uppercase;
            letter-spacing: 3px;
            font-weight: bold;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
        }

        nav {
            position: sticky;
            top: 0;
            background: rgba(0, 0, 0, 0.7);
            padding: 15px 0;
            z-index: 1000;
            transition: background-color 0.3s;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 25px;
            font-size: 1.2em;
            text-transform: uppercase;
            font-weight: 600;
            letter-spacing: 1px;
            padding: 5px 0;
        }

        nav a::after {
            content: '';
            position: absolute;
            width: 0%;
            height: 2px;
            background: #9b59b6;
            transition: width 0.3s ease;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }

        nav a:hover::after {
            width: 100%;
        }

        nav a:hover {
            color: #9b59b6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 50px auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.5s ease;
        }

        .container:hover {
            transform: translateY(-10px);
        }

        .section {
            padding: 40px 30px;
            border-bottom: 2px solid #eee;
        }

        .section:last-child {
            border-bottom: none;
        }

        .section h2 {
            font-size: 2.5em;
            color: #8e44ad;
            margin-bottom: 20px;
            text-transform: uppercase;
            font-weight: 600;
            letter-spacing: 2px;
        }

        .section p, .section ul {
            font-size: 1.2em;
            color: #555;
        }

        .section ul {
            list-style-type: none;
            padding-left: 20px;
        }

        .section li {
            margin-bottom: 10px;
        }

        footer {
            background: #8e44ad;
            color: white;
            padding: 20px 0;
            text-align: center;
            font-size: 1.2em;
            letter-spacing: 2px;
        }

        footer p {
            margin: 0;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2.5em;
            }

            nav a {
                margin: 0 15px;
                font-size: 1.1em;
            }

            .container {
                width: 95%;
            }
        }

        .slider {
            position: relative;
            width: 100%;
            max-width: 1200px;
            margin: 50px auto;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .slides {
            display: flex;
            transition: transform 1s ease;
        }

        .slide {
            width: 100%;
            height: 400px;
            background-position: center;
            background-size: cover;
        }

        .slide:nth-child(1) {
            background-image: url('https://via.placeholder.com/1200x400/8e44ad/ffffff?text=білім');
        }

        .slide:nth-child(2) {
            background-image: url('https://via.placeholder.com/1200x400/6c3483/ffffff?text=және');
        }

        .slide:nth-child(3) {
            background-image: url('https://via.placeholder.com/1200x400/9b59b6/ffffff?text=даму');
        }

        .slider-buttons {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }

        .slider-button {
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 10px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .slider-button:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            padding-top: 60px;
        }

        .modal-content {
            background-color: #fff;
            margin: 5% auto;
            padding: 20px;
            border-radius: 8px;
            width: 80%;
            max-width: 600px;
            animation: fadeIn 1s ease;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>№ 135 А.Тоқмағанбетов атындағы орта мектеп</h1>
        <p>Білім орталығы</p>
    </header>

    <nav>
        <a href="#about">Мектеп туралы</a>
        <a href="#teachers">Мұғалімдер</a>
        <a href="#students">Оқушылар жетістіктері</a>
        <a href="#contact">Байланыс</a>
    </nav>

    <div class="container">
        <div class="slider">
            <div class="slides">
                <div class="slide"></div>
                <div class="slide"></div>
                <div class="slide"></div>
            </div>
            <div class="slider-buttons">
                <button class="slider-button" id="prevSlide">&#10094;</button>
                <button class="slider-button" id="nextSlide">&#10095;</button>
            </div>
        </div>
        
        <div class="section" id="about">
            <h2>Мектеп туралы</h2>
            <p>135 А.Тоқмағанбетов атындағы орта мектеп — еліміздің ең үздік білім ордасы. Біздің мақсатымыз — оқушыларға сапалы білім беру арқылы оларды болашаққа дайындау. Мектептің тарихы - «Молотов» атындағы жеті жылдық мектеп Елімізде 50-жылдардың басында колхоздарды ірілендіру жүзеге асырылды. Біздің ауылымызда көрші отырған төрт майда колхоздар: Майлықұм, XVIII партсъезд, Бидайкөл, Қызылорақ бірігіп 1950 жылы XVIII партсъезд колхозы болып аталып іріленді. Майлықұм колхозындағы «Молотов» атындағы жеті жылдық XVIII партсъезд колхозындағы «Н.К.Крупская» атындағы жеті жылдық және Бидайкөл колхозындағы бастауыш мектептер бірігіп 1950-51 оқу жылында «Молотов» атындағы жеті жылдық  мектеп болып аталды. Ол кезде мектеп шағын болатын. Мектеп директоры Жәрекеев Төлеп жолдас еді. 1952-53 оқу жылында Дауылбаев Әлмағанбет, 1954-55 оқу жылынан бастап Өтеков Нұрғали жолдастар мектеп директоры болып жұмыс істеді. 1956-57 оқу жылынан бастап 1961-62 оқу жылының аяғына дейін Жұқабаев Дүйсен мектепті басқарды.  Мектеп түлектері республикаға еңбегі сіңген қызметкер, режиссер Хүсейін Теміров, Қазақстан суретшілер одағының мүшесі Сәменов Шәкен еді. «Партияның  XVIII съезі» атындағы жеті жылдық мектеп 1957 жыл тамыз айынан бастап мектептің аты «Партияның XVIII съезі» атындағы жеті жылдық мектеп болып өзгерді де, 1960-61 оқу жылынан сегіз жылдық мектепке айналды. 1962-63 оқу жылынан Досымов Төлеген, 1965-66 оқу жылынан Алданазаров Рүстембек, 1967-68 оқу жылынан Омаров Абдолла, 1969-70 оқу жылынан Бисенов Жолшыбек мектеп директоры болып жұмыс істеді. Мектеп 1969-70 оқу жылынан бастап орта мектепке айналды да, 1970-71 оқу жылында бірінші рет орта білім алушыларды  мектеп қабырғасынан түлетіп ұшырды. 1973 жылы мектеп қабырғасынан түлеп ұшқан қазіргі «Гүлдер» ансамблінің жетекшісі, продюссер Ибрашева Сарсен, педагогика ғылымының кандидаты Төлегенов Шаһарбек, І-санатты дәрігер-терапевт Раманқұлова Тәжігүл еді. 1976-1977 жылдан бастап Шілманов Бабаомар мектеп директоры болып, мектепті алтын медальмен Әбдірәсілова Күлжан мен Сардарбекова Гүлсім тәмәмдады. Сол жылдары мектеп дружинасы «Оң қанатты дружина» атағын алып жүрді. 1977-78 бен 1978-1979 оқу жылдары Божанова Алмагүл басқарып, мектепті Уайсова Айзада алтын медальмен аяқтады. Мектепке 1984 жылдан бастап Қазақ ССР-і Министрлер кабинетінің шешімімен ақын, сатирик Асқар Тоқмағамбетов есімі берілді.</p>
            <p><center>Соғыс ардагерлерінің мұғалім кездері</center> </p>
            <img src="222.jpg" class="photo-left">
            <img src="333.jpg" class="photo-right">
            <img src="444.jpg" class="photo-left">
            <img src="111.jpg" alt="" class="photo-right">
         </div>

        <div class="section" id="teachers">
            <h2>Мектеп директоры және завучтар</h2>
            <ul>
                <li>
                    <img src="135.jpg" alt="Сурет" style="width: 330px; height: 330px; vertical-align: middle; margin-right: 10px;">
                    Нұрлан Құрманәлиев - 2019 жылдан бастап мектеп директоры
                </li>
            </ul>
        </div>

        <div class="section" id="students">
            <h2>Оқушылар жетістіктері</h2>
            <ul>
                <li>Ақылбеков Нұртөре 10 сынып оқушысы - ауыл олимпиадасының облыстық кезеңінің жүлдегері және Айқанат Республикалық олимпиаданың соңғы кезеңінің қатысушысы,мектебіміздің басты мақтанышы.</li>
            </ul>
        </div>

        <div class="section" id="contact">
            <h2>Байланыс</h2>
            <p>Мекен-жайы: 135, Қызылорда облысы Сырдария ауданы Тереңөзек кенті Асқар Тоқмағанбетов ауылы</p>
            <p>Телефон нөмірі: 8 771 339 98 24</p>
            <button id="contactModalBtn">Қосымша ақпарат</button>
        </div>
    </div>

    <div id="contactModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Қосымша ақпарат</h2>
            <p>Мектепке келу үшін төмендегі мекен-жай бойынша хабарласуға болады:</p>
            <p>Телефон номері: 8 771 339 98 24</p>
        </div>
    </div>

    <footer>
        <p>135 А.Тоқмағанбетов атындағы орта мектеп. Барлық құқықтар қорғалған.</p>
    </footer>

    <script>
        var modal = document.getElementById("contactModal");
        var btn = document.getElementById("contactModalBtn");
        var span = document.getElementsByClassName("close")[0];

        btn.onclick = function() {
            modal.style.display = "block";
        }

        span.onclick = function() {
            modal.style.display = "none";
        }

        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }

        var currentSlide = 0;
        var slides = document.querySelector(".slides");
        var totalSlides = document.querySelectorAll(".slide").length;

        document.getElementById("nextSlide").onclick = function() {
            currentSlide = (currentSlide + 1) % totalSlides;
            slides.style.transform = "translateX(-" + currentSlide * 100 + "%)";
        }

        document.getElementById("prevSlide").onclick = function() {
            currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
            slides.style.transform = "translateX(-" + currentSlide * 100 + "%)";
        }
    </script>
</body>
</html>
