/* تصفية المارجين والبادينج لكل العناصر */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* إعدادات الجسم وتوسيط المحتوى */
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
    color: #333;
    background-image: url('https://i.pinimg.com/originals/a5/d6/cd/a5d6cd9a56002a90e04c90e9be8c3a1d.gif'); /* خلفية قلوب متحركة */
    background-size: 100px 100px;
    background-repeat: repeat;
    overflow: hidden;
}

/* الحاوية الرئيسية لتوسيط العناصر */
.container {
    text-align: center;
}

/* تنسيق القلب ليكون باللون الأحمر وبحجم كبير */
.heart {
    font-size: 100px;
    color: red;
    cursor: pointer;
    transition: transform 0.3s ease;
}

/* تأثير عند التمرير فوق القلب (تكبيره) */
.heart:hover {
    transform: scale(1.2);
}

/* إخفاء النص في البداية */
.hidden {
    display: none;
}

/* تنسيق النص عند ظهوره */
#message {
    margin-top: 20px;
    font-size: 24px;
    color: #ff3366;
    font-weight: bold;
}

/* تأثيرات الألوان عند الضغط على القلب */
@keyframes colorBurst {
    0% {
        transform: scale(1);
        opacity: 1;
    }
    100% {
        transform: scale(2);
        opacity: 0;
    }
}

.burst {
    position: absolute;
    animation: colorBurst 1s forwards;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background: radial-gradient(circle, red, yellow, blue, green);
    opacity: 0;
}
