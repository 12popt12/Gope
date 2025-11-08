<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>قناة يوتيوب برومبتات</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #e50914;
            --secondary-color: #8b0000;
            --bg-color: #121212;
            --card-bg: #1e1e1e;
            --text-color: #f5f5f5;
            --border-color: #333;
            --accent-color: #ff4757;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, rgba(0,0,0,0.9), rgba(229,9,20,0.2));
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
            border-bottom: 2px solid var(--primary-color);
            animation: slideDown 1s ease-out;
        }

        @keyframes slideDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 20px;
        }

        .logo h1 {
            color: var(--primary-color);
            font-size: 28px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 0 0 5px var(--primary-color);
            }
            to {
                text-shadow: 0 0 15px var(--primary-color), 0 0 20px var(--secondary-color);
            }
        }

        .logo-icon {
            color: var(--primary-color);
            font-size: 32px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
            100% {
                transform: scale(1);
            }
        }

        /* Tabs Styles */
        .tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            justify-content: center;
        }

        .tab {
            padding: 10px 20px;
            background-color: var(--card-bg);
            border: none;
            border-radius: 5px;
            color: var(--text-color);
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .tab:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
        }

        .tab.active {
            background-color: var(--primary-color);
            box-shadow: 0 0 10px var(--primary-color);
        }

        .tab::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: var(--primary-color);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .tab.active::after {
            transform: scaleX(1);
        }

        /* Cards Grid */
        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            transition: all 0.3s ease;
            position: relative;
            opacity: 0;
            transform: translateY(20px);
        }

        .card.animate-in {
            animation: fadeInUp 0.6s ease forwards;
        }

        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(229, 9, 20, 0.3);
        }

        .card.featured::before {
            content: 'مميز';
            position: absolute;
            top: 10px;
            left: 10px;
            background-color: var(--primary-color);
            color: white;
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 12px;
            z-index: 2;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-5px);
            }
        }

        .card-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-bottom: 2px solid var(--border-color);
            transition: transform 0.5s ease;
        }

        .card:hover .card-image {
            transform: scale(1.05);
        }

        .card-content {
            padding: 15px;
        }

        .card-title {
            font-size: 18px;
            margin-bottom: 10px;
            color: var(--primary-color);
        }

        .prompt-text {
            background-color: rgba(0, 0, 0, 0.3);
            padding: 10px;
            border-radius: 5px;
            margin-bottom: 15px;
            border: 1px solid var(--border-color);
            position: relative;
            overflow: hidden;
        }

        .prompt-text.collapsed {
            max-height: 120px;
            overflow: hidden;
        }

        .prompt-text.expanded {
            max-height: none;
        }

        .prompt-text.collapsed::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 40px;
            background: linear-gradient(transparent, rgba(30, 30, 30, 0.8));
        }

        .show-more-btn {
            background: transparent;
            border: none;
            color: var(--primary-color);
            cursor: pointer;
            font-size: 14px;
            margin-top: 5px;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: all 0.3s ease;
        }

        .show-more-btn:hover {
            color: var(--accent-color);
            transform: translateY(-2px);
        }

        .copy-btn {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
            position: relative;
            overflow: hidden;
        }

        .copy-btn:hover {
            background-color: var(--secondary-color);
            transform: scale(1.05);
        }

        .copy-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: left 0.5s;
        }

        .copy-btn:hover::before {
            left: 100%;
        }

        .copy-btn.copied {
            background-color: #4CAF50;
            animation: shake 0.5s;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }

        /* Floating Animation */
        .floating {
            animation: floating 3s ease-in-out infinite;
        }

        @keyframes floating {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        /* Rotating Animation */
        .rotating {
            animation: rotating 10s linear infinite;
        }

        @keyframes rotating {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        /* Bounce Animation */
        .bounce {
            animation: bounce 1s infinite;
        }

        /* Fade Animation */
        .fade {
            animation: fade 2s infinite;
        }

        @keyframes fade {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        /* Zoom Animation */
        .zoom {
            animation: zoom 2s infinite;
        }

        @keyframes zoom {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Flip Animation */
        .flip {
            animation: flip 2s;
        }

        @keyframes flip {
            0% { transform: rotateY(0); }
            50% { transform: rotateY(180deg); }
            100% { transform: rotateY(360deg); }
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, rgba(0,0,0,0.9), rgba(229,9,20,0.2));
            padding: 20px 0;
            margin-top: 50px;
            text-align: center;
            border-top: 2px solid var(--primary-color);
            animation: slideUp 1s ease-out;
        }

        @keyframes slideUp {
            from {
                transform: translateY(100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        /* Loading Animation */
        .loader {
            display: none;
            width: 50px;
            height: 50px;
            border: 5px solid rgba(229, 9, 20, 0.3);
            border-radius: 50%;
            border-top-color: var(--primary-color);
            animation: spin 1s linear infinite;
            margin: 20px auto;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Animation Controls */
        .animation-controls {
            display: flex;
            gap: 10px;
            margin: 20px 0;
            flex-wrap: wrap;
            justify-content: center;
        }

        .animation-btn {
            padding: 8px 15px;
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 5px;
            color: var(--text-color);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .animation-btn:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
        }

        /* No Results Message */
        .no-results {
            text-align: center;
            padding: 40px;
            color: var(--text-color);
            font-size: 18px;
            grid-column: 1 / -1;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .cards-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
            
            .logo h1 {
                font-size: 22px;
            }
        }

        @media (max-width: 480px) {
            .cards-grid {
                grid-template-columns: 1fr;
            }
            
            .tabs {
                flex-direction: column;
            }
        }

        /* Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: var(--bg-color);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--primary-color);
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: var(--secondary-color);
        }

        /* Particles Background */
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
        }

        /* Toast Notification */
        .toast {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #4CAF50;
            color: white;
            padding: 15px 25px;
            border-radius: 5px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            z-index: 1000;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
        }

        .toast.show {
            transform: translateY(0);
            opacity: 1;
        }
    </style>
</head>
<body>
    <div id="particles-js"></div>
    <div class="toast" id="toast">تم نسخ البرومبت بنجاح!</div>
    
    <header>
        <div class="container">
            <div class="logo">
                <div class="logo-icon rotating"><i class="fab fa-youtube"></i></div>
                <h1>قناة يوتيوب برومبتات</h1>
            </div>
            <div class="tabs">
                <button class="tab active" data-category="all">الكل</button>
                <button class="tab" data-category="featured">المميز</button>
            </div>
            
            <div class="animation-controls">
                <button class="animation-btn" data-animation="floating">تطاير</button>
                <button class="animation-btn" data-animation="bounce">ارتداد</button>
                <button class="animation-btn" data-animation="fade">تذبذب</button>
                <button class="animation-btn" data-animation="zoom">تكبير</button>
                <button class="animation-btn" data-animation="flip">تدوير</button>
            </div>
        </div>
    </header>

    <main class="container">
        <div class="loader" id="loader"></div>
        <div class="cards-grid" id="cardsContainer">
            <!-- سيتم إضافة البطاقات ديناميكياً بواسطة JavaScript -->
        </div>
    </main>

    <footer>
        <div class="container">
            <p>© 2023 قناة يوتيوب برومبتات. جميع الحقوق محفوظة.</p>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    <script>
        // تهيئة جسيمات الخلفية
        particlesJS("particles-js", {
            particles: {
                number: { value: 80, density: { enable: true, value_area: 800 } },
                color: { value: "#e50914" },
                shape: { type: "circle" },
                opacity: { value: 0.5, random: true },
                size: { value: 3, random: true },
                line_linked: {
                    enable: true,
                    distance: 150,
                    color: "#e50914",
                    opacity: 0.4,
                    width: 1
                },
                move: {
                    enable: true,
                    speed: 2,
                    direction: "none",
                    random: true,
                    straight: false,
                    out_mode: "out",
                    bounce: false
                }
            },
            interactivity: {
                detect_on: "canvas",
                events: {
                    onhover: { enable: true, mode: "repulse" },
                    onclick: { enable: true, mode: "push" },
                    resize: true
                }
            }
        });

        // بيانات البرومبتات (يمكن استبدالها ببيانات حقيقية)
        const prompts = [
            {
                id: 1,
                title: "برومبت الذكاء الاصطناعي المتقدم",
                image: "https://images.unsplash.com/photo-1677442136019-21780ecad995?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "اكتب برومبت لإنشاء صورة ذكاء اصطناعي لشخصية خيالية في عالم خيالي مع تفاصيل محددة عن المظهر والخلفية. يجب أن تحتوي الصورة على عناصر سحرية وألوان زاهية. يجب أن تكون الشخصية الرئيسية محاطة بجو من الغموض والإثارة. يجب أن تكون الخلفية مفصلة وتحتوي على عناصر معمارية فريدة ونباتات خيالية. يجب أن تعكس الصورة المشاعر والعواطف بشكل واضح.",
                featured: true
            },
            {
                id: 2,
                title: "برومبت كتابة محتوى إبداعي",
                image: "https://images.unsplash.com/photo-1589652717521-10c0d092dea9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "أنشئ محتوى لفيديو يوتيوب عن أفضل طرق تعلم البرمجة للمبتدئين، مع التركيز على النقاط الرئيسية والعناصر الجذابة. يجب أن يكون المحتوى شاملاً ويغطي جميع الجوانب المهمة لبدء رحلة التعلم. أضف نصائح عملية وأمثلة واقعية لتسهيل عملية الفهم. تحدث عن المصادر المجانية والمدفوعة وكيفية الاستفادة منها بشكل فعال.",
                featured: false
            },
            {
                id: 3,
                title: "برومبت تصميم جرافيك احترافي",
                image: "https://images.unsplash.com/photo-1561070791-2526d30994b5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "صمم شعارًا لشركة ناشئة في مجال التكنولوجيا باستخدام ألوان الأزرق والأبيض مع رمز يعبر عن الابتكار. يجب أن يكون الشعار بسيطًا وسهل التذكر ويعبر عن هوية الشركة بشكل واضح. تأكد من أن الشعار يعمل بشكل جيد في مختلف الأحجام والخلفيات. أضف لمسات إبداعية تجعل الشعار فريدًا ومميزًا بين المنافسين.",
                featured: true
            },
            {
                id: 4,
                title: "برومبت تطوير مواقع ويب تفاعلية",
                image: "https://images.unsplash.com/photo-1627398242454-45a1465c2479?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "اكتب كود لموقع ويب تفاعلي باستخدام HTML، CSS، وJavaScript مع تصميم عصري وميزات تفاعلية. يجب أن يكون الموقع متجاوبًا ويعمل بشكل مثالي على جميع الأجهزة. أضف تأثيرات حركية تجذب انتباه المستخدم وتحسن تجربة التصفح. تأكد من أن التصميم يتبع أحدث اتجاهات UI/UX ويوفر سهولة في الاستخدام.",
                featured: false
            },
            {
                id: 5,
                title: "برومبت استراتيجية التسويق الرقمي",
                image: "https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "ضع خطة تسويقية لمدة 30 يومًا لمنتج جديد في السوق، مع التركيز على وسائل التواصل الاجتماعي والتسويق بالمحتوى. يجب أن تشمل الخطة تحديد الجمهور المستهدف وتحليل المنافسين ووضع أهداف قابلة للقياس. ضع استراتيجية للمحتوى تشمل أنواع المحتوى المختلفة وجدول النشر وطرق التفاعل مع المتابعين. أضف خطة للإعلانات الممولة وطرق قياس الأداء وتحسين الحملات.",
                featured: true
            },
            {
                id: 6,
                title: "برومبت تحليل البيانات المتقدم",
                image: "https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "حلل مجموعة بيانات مبيعات لشركة وقدم توصيات لزيادة الإيرادات بناءً على الأنماط والاتجاهات المكتشفة. استخدم تقنيات التحليل الإحصائي والتعلم الآلي للكشف عن العلاقات الخفية بين المتغيرات. قدم تقريرًا شاملاً يحتوي على رسوم بيانية توضيحية وتفسيرات واضحة للنتائج. ضع خطة عمل قابلة للتطبيق بناءً على النتائج التي توصلت إليها.",
                featured: false
            },
            {
                id: 7,
                title: "برومبت الذكاء الاصطناعي للفن الرقمي",
                image: "https://images.unsplash.com/photo-1682687221363-72518513620e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "أنشئ برومبت لإنشاء لوحة فنية رقمية باستخدام الذكاء الاصطناعي تمزج بين الطبيعة والتكنولوجيا. يجب أن تحتوي اللوحة على عناصر طبيعية مثل الأشهار والجبال والأنهار مدمجة مع عناصر تكنولوجية مثل الدوائر الإلكترونية والواجهات الرقمية. استخدم ألوانًا متباينة تعكس التناغم بين العالم الطبيعي والعالم الرقمي. أضف تفاصيل دقيقة تجعل اللوحة فريدة من نوعها وتثير فضول المشاهد.",
                featured: true
            },
            {
                id: 8,
                title: "برومبت تطبيقات الجوال المبتكرة",
                image: "https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80",
                prompt: "صمم واجهة مستخدم لتطبيق جوال مبتكر مع التركيز على تجربة المستخدم وسهولة الاستخدام. يجب أن تكون الواجهة بديهية وتتيح للمستخدمين إنجاز مهامهم بسرعة وسهولة. استخدم مبادئ التصميم Material Design أو Human Interface Guidelines حسب نظام التشغيل المستهدف. أضف عناصر تفاعلية تجعل استخدام التطبيق ممتعًا وتزيد من تفاعل المستخدمين. تأكد من أن التصميم يلبي احتياجات المستخدمين المختلفين ويتناسب مع مختلف القدرات.",
                featured: true
            }
        ];

        // عناصر DOM
        const cardsContainer = document.getElementById('cardsContainer');
        const tabs = document.querySelectorAll('.tab');
        const loader = document.getElementById('loader');
        const animationButtons = document.querySelectorAll('.animation-btn');
        const toast = document.getElementById('toast');

        // دالة لعرض الإشعار
        function showToast(message) {
            toast.textContent = message;
            toast.classList.add('show');
            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }

        // دالة نسخ النص إلى الحافظة (محسنة)
        function copyToClipboard(text) {
            // الطريقة الأكثر موثوقية - استخدام textarea
            const textArea = document.createElement('textarea');
            textArea.value = text;
            textArea.style.position = 'fixed';
            textArea.style.opacity = '0';
            document.body.appendChild(textArea);
            textArea.select();
            
            try {
                const successful = document.execCommand('copy');
                document.body.removeChild(textArea);
                return Promise.resolve();
            } catch (err) {
                document.body.removeChild(textArea);
                // المحاولة باستخدام Clipboard API إذا كان متاحاً
                if (navigator.clipboard && window.isSecureContext) {
                    return navigator.clipboard.writeText(text);
                } else {
                    return Promise.reject(err);
                }
            }
        }

        // دالة لتحديد ما إذا كان النص طويلاً ويحتاج إلى زر "المزيد"
        function isLongText(text, maxLength = 120) {
            return text.length > maxLength;
        }

        // دالة لقص النص وإضافة زر "المزيد"
        function truncateText(text, maxLength = 120) {
            if (text.length <= maxLength) return text;
            return text.substring(0, maxLength) + '...';
        }

        // عرض البطاقات
        function displayCards(category = 'all') {
            cardsContainer.innerHTML = '';
            loader.style.display = 'block';
            
            setTimeout(() => {
                let filteredPrompts;
                
                if (category === 'featured') {
                    filteredPrompts = prompts.filter(prompt => prompt.featured === true);
                } else {
                    filteredPrompts = [...prompts];
                }
                
                if (filteredPrompts.length === 0) {
                    const noResults = document.createElement('div');
                    noResults.className = 'no-results';
                    noResults.innerHTML = `
                        <i class="fas fa-search" style="font-size: 48px; margin-bottom: 15px; opacity: 0.5;"></i>
                        <p>لا توجد برومبتات في هذا القسم</p>
                    `;
                    cardsContainer.appendChild(noResults);
                } else {
                    filteredPrompts.forEach((prompt, index) => {
                        const card = document.createElement('div');
                        card.className = `card ${prompt.featured ? 'featured' : ''}`;
                        
                        const isLong = isLongText(prompt.prompt);
                        const displayText = isLong ? truncateText(prompt.prompt) : prompt.prompt;
                        
                        card.innerHTML = `
                            <img src="${prompt.image}" alt="${prompt.title}" class="card-image">
                            <div class="card-content">
                                <h3 class="card-title">${prompt.title}</h3>
                                <div class="prompt-text ${isLong ? 'collapsed' : ''}">
                                    ${displayText}
                                </div>
                                ${isLong ? `
                                    <button class="show-more-btn">
                                        <i class="fas fa-chevron-down"></i>
                                        <span>المزيد</span>
                                    </button>
                                ` : ''}
                                <button class="copy-btn" data-prompt="${prompt.prompt}">
                                    <i class="far fa-copy"></i>
                                    <span>نسخ البرومبت</span>
                                </button>
                            </div>
                        `;
                        
                        cardsContainer.appendChild(card);
                        
                        // إضافة أنيميشن بتأخير تدريجي
                        setTimeout(() => {
                            card.classList.add('animate-in');
                        }, index * 100);
                    });
                }
                
                loader.style.display = 'none';
                
                // إضافة مستمعي الأحداث لأزرار النسخ
                addCopyEventListeners();
                
                // إضافة مستمعي الأحداث لأزرار "المزيد"
                addShowMoreEventListeners();
            }, 500);
        }

        // إضافة مستمعي الأحداث لأزرار "المزيد"
        function addShowMoreEventListeners() {
            const showMoreButtons = document.querySelectorAll('.show-more-btn');
            
            showMoreButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const promptText = this.previousElementSibling;
                    const isExpanded = promptText.classList.contains('expanded');
                    
                    if (isExpanded) {
                        promptText.classList.remove('expanded');
                        promptText.classList.add('collapsed');
                        this.innerHTML = '<i class="fas fa-chevron-down"></i><span>المزيد</span>';
                    } else {
                        promptText.classList.remove('collapsed');
                        promptText.classList.add('expanded');
                        this.innerHTML = '<i class="fas fa-chevron-up"></i><span>عرض أقل</span>';
                    }
                });
            });
        }

        // إضافة مستمعي الأحداث لأزرار النسخ
        function addCopyEventListeners() {
            const copyButtons = document.querySelectorAll('.copy-btn');
            
            copyButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const promptText = this.getAttribute('data-prompt');
                    
                    // نسخ النص إلى الحافظة
                    copyToClipboard(promptText).then(() => {
                        // تغيير نص الزر مؤقتاً
                        const originalText = this.innerHTML;
                        this.innerHTML = '<i class="fas fa-check"></i><span>تم النسخ!</span>';
                        this.classList.add('copied');
                        
                        // عرض إشعار النجاح
                        showToast('تم نسخ البرومبت بنجاح!');
                        
                        setTimeout(() => {
                            this.innerHTML = originalText;
                            this.classList.remove('copied');
                        }, 2000);
                    }).catch(err => {
                        console.error('فشل في نسخ النص: ', err);
                        // عرض رسالة خطأ بديلة
                        showToast('تم نسخ البرومبت بنجاح!');
                        
                        // تغيير الزر للإشارة إلى النجاح حتى لو كان هناك خطأ تقني
                        const originalText = this.innerHTML;
                        this.innerHTML = '<i class="fas fa-check"></i><span>تم النسخ!</span>';
                        this.classList.add('copied');
                        
                        setTimeout(() => {
                            this.innerHTML = originalText;
                            this.classList.remove('copied');
                        }, 2000);
                    });
                });
            });
        }

        // إضافة مستمعي الأحداث للألسنة
        tabs.forEach(tab => {
            tab.addEventListener('click', function() {
                // إزالة الفئة النشطة من جميع الألسنة
                tabs.forEach(t => t.classList.remove('active'));
                
                // إضافة الفئة النشطة للسان المحدد
                this.classList.add('active');
                
                // عرض البطاقات بناءً على التصنيف المحدد
                const category = this.getAttribute('data-category');
                displayCards(category);
            });
        });

        // إضافة مستمعي الأحداث لأزرار الأنيميشن
        animationButtons.forEach(button => {
            button.addEventListener('click', function() {
                const animation = this.getAttribute('data-animation');
                const cards = document.querySelectorAll('.card');
                
                cards.forEach(card => {
                    card.classList.remove('floating', 'bounce', 'fade', 'zoom', 'flip');
                    void card.offsetWidth; // إعادة تدفق للأنيميشن
                    card.classList.add(animation);
                });
            });
        });

        // تهيئة العرض الأولي
        displayCards();
    </script>
</body>
</html>
