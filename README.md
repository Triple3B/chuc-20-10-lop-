<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chúc Mừng 20/10 - 13 Nàng Công Chúa Lớp Tôi! ❤️</title>
    <style>
        /* CSS Cơ bản (Giữ nguyên từ bản trước để đảm bảo hiệu ứng) */
        body {
            font-family: 'Times New Roman', serif;
            margin: 0;
            padding: 0;
            background-color: #e8f5e9; 
            color: #388e3c; 
            text-align: center;
            overflow-x: hidden;
        }

        /* Phần Màn hình Chào mừng */
        #welcome-screen {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #4db6ac; 
            color: white;
            transition: opacity 1s ease-in-out;
            position: relative;
        }

        #welcome-screen h1 {
            font-size: 2.8em;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
            40% {transform: translateY(-15px);}
            60% {transform: translateY(-7px);}
        }

        #start-button {
            padding: 18px 35px;
            font-size: 1.6em;
            cursor: pointer;
            background-color: #ff6f61; 
            color: white;
            border: 3px solid white;
            border-radius: 50px;
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.3);
            transition: all 0.3s ease;
            font-weight: bold;
        }

        #start-button:hover {
            background-color: #e55a4f;
            transform: scale(1.05);
        }

        /* Phần Nội dung Chính */
        #main-content {
            display: none;
            padding: 40px 20px;
            background: linear-gradient(135deg, #f0f0f0, #e0e0e0);
        }

        .header-text {
            color: #d84315; 
            margin-bottom: 30px;
            font-size: 2.5em;
            font-weight: 700;
        }

        .student-card {
            background-color: white;
            border-radius: 20px;
            padding: 30px;
            margin: 40px auto;
            max-width: 700px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
            transition: transform 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            border: 2px solid #ffab91;
            overflow: hidden;
        }

        .student-card:hover {
            transform: scale(1.02);
        }

        .student-card h2 {
            color: #880e4f;
            margin-top: 0;
            font-size: 2.2em;
            border-bottom: 2px dashed #ffe0b2;
            padding-bottom: 10px;
        }

        .student-image {
            width: 250px;
            height: auto;
            max-height: 250px;
            object-fit: cover;
            border-radius: 15px;
            border: 5px solid #ffccbc; 
            margin-bottom: 20px;
        }
        
        /* CSS cho ảnh đặc biệt - Bóng đổ */
        .shadow-image {
            border-radius: 15px;
            border: none;
            width: 90%;
            max-width: 400px;
            height: auto;
            margin-top: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.4);
        }


        .congratulations {
            font-style: italic;
            font-size: 1.3em;
            color: #1b5e20; 
            line-height: 1.7;
            padding: 15px;
            background-color: #f1f8e9;
            border-radius: 10px;
            margin-top: 20px;
        }

        /* Hiệu ứng Trái tim Bay */
        .heart {
            position: fixed;
            top: -10vh;
            font-size: 2.5em;
            color: #ff0066;
            animation: fall linear infinite;
            pointer-events: none;
            z-index: 1000;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
        }

        @keyframes fall {
            to {
                transform: translateY(105vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* Các ảnh nhỏ hiển thị đầu tiên */
        .preview-images {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 25px;
        }

        .preview-images img {
            width: 90px;
            height: 90px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #f48fb1; 
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }
        
        .preview-images img:hover {
            transform: rotate(-5deg) scale(1.1);
        }
        
    </style>
</head>
<body>

    <audio id="myAudio" loop>
        <source src="khi_em_lon.mp3" type="audio/mp3"> 
        Trình duyệt của bạn không hỗ trợ thẻ audio.
    </audio>

    <div id="welcome-screen">
        <h1>Mở Món Quà Âm Nhạc Gửi Đến 13 "Nàng Thơ" Lớp Ta! 🎁</h1>
        <p style="font-size: 1.2em; color: #e0f2f1;">Nhạc nền: **Khi Em Lớn** (Orange & Hoàng Dũng)</p>
        <button id="start-button">START ✨</button>
    </div>

    <div id="main-content">
        <h1 class="header-text">👑 Chúc Mừng 13 Cô Gái Tuyệt Vời Của Lớp! 👑</h1>
        
        <div id="student-list">
            </div>
    </div>

    <script>
        // --- DỮ LIỆU CỦA 13 BẠN NỮ (BẠN PHẢI CHỈNH SỬA THÔNG TIN Ở ĐÂY) ---
        const students = [
            // BẠN SỐ 1 (ĐẶC BIỆT - Dùng ảnh bóng đổ bạn cung cấp)
            {
                name: "Thùy Linh (Nàng Thơ Lớp Ta)",
                image: "z4726366898513_5a93b6f320a036a29fd9bd9cafdd28ea.jpg", 
                isShadow: true, 
                congratulation: "Gửi cô gái luôn mang sự dịu dàng và bí ẩn như ánh trăng. Chúc Linh 20/10 thật hạnh phúc, rạng rỡ, và mãi là nguồn cảm hứng cho những điều tuyệt vời nhất!"
            },
            // BẠN SỐ 2
            {
                name: "Ngọc Mai",
                image: "path/to/image_02.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Chúc Mai luôn xinh đẹp, tự tin tỏa sáng và đạt được mọi mục tiêu học tập. Bạn chính là niềm tự hào của lớp mình!"
            },
            // BẠN SỐ 3
            {
                name: "Phương Lan",
                image: "path/to/image_03.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Lan ơi, cảm ơn bạn đã luôn nhiệt huyết và dẫn dắt lớp. Chúc bạn một ngày 20/10 ấm áp, nhiều niềm vui và luôn giữ vững phong độ nhé!"
            },
            // BẠN SỐ 4
            {
                name: "Thanh Hà",
                image: "path/to/image_04.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Hà cô gái năng động, chúc bạn luôn giữ được nụ cười tươi tắn và đón nhận thật nhiều niềm vui trong ngày đặc biệt này!"
            },
            // BẠN SỐ 5
            {
                name: "Ánh Nguyệt",
                image: "path/to/image_05.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Nguyệt ơi, chúc bạn 20/10 thật nhiều quà, luôn ngọt ngào và đáng yêu như bây giờ. Hãy tỏa sáng theo cách của riêng bạn!"
            },
            // BẠN SỐ 6
            {
                name: "Kim Ngân",
                image: "path/to/image_06.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Chúc Ngân luôn mạnh mẽ, quyết đoán và chinh phục mọi thử thách. Chúc mừng Ngày Phụ nữ Việt Nam!"
            },
            // BẠN SỐ 7
            {
                name: "Minh Châu",
                image: "path/to/image_07.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Châu là cô gái tinh tế và đáng mến. Chúc bạn luôn an yên, hạnh phúc và nhận được tất cả những điều tốt đẹp nhất!"
            },
            // BẠN SỐ 8
            {
                name: "Diệu Hương",
                image: "path/to/image_08.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Gửi Hương những lời chúc chân thành nhất. Chúc bạn 20/10 ý nghĩa, mãi là cô gái ấm áp và dịu dàng của lớp!"
            },
            // BẠN SỐ 9
            {
                name: "Bảo Trâm",
                image: "path/to/image_09.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Trâm ơi, hãy luôn tự tin với tài năng và cá tính của mình nhé. Chúc mừng bạn nhân ngày 20/10!"
            },
            // BẠN SỐ 10
            {
                name: "Khánh Huyền",
                image: "path/to/image_10.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Chúc Huyền luôn vui vẻ, học tập thật tốt và mọi điều ước nhỏ xinh đều trở thành hiện thực!"
            },
            // BẠN SỐ 11
            {
                name: "Thu Hoài",
                image: "path/to/image_11.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Gửi Hoài những đóa hoa tươi thắm nhất. Chúc bạn một ngày 20/10 tràn ngập tiếng cười và những bất ngờ thú vị!"
            },
            // BẠN SỐ 12
            {
                name: "Yến Nhi",
                image: "path/to/image_12.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Nhi là cô gái chăm chỉ và đáng ngưỡng mộ. Chúc bạn luôn giữ vững tinh thần này và nhận được thật nhiều yêu thương!"
            },
            // BẠN SỐ 13
            {
                name: "Mỹ Hạnh",
                image: "path/to/image_13.jpg", // **THAY THẾ BẰNG ẢNH THẬT**
                isShadow: false,
                congratulation: "Chúc Hạnh có một ngày 20/10 thật đáng nhớ, luôn xinh đẹp và là chính mình! Happy Vietnamese Women's Day!"
            }
        ];
        
        // --- CHỨC NĂNG CHÍNH (GIỮ NGUYÊN) ---
        const startButton = document.getElementById('start-button');
        const welcomeScreen = document.getElementById('welcome-screen');
        const mainContent = document.getElementById('main-content');
        const myAudio = document.getElementById('myAudio');
        const studentListDiv = document.getElementById('student-list');

        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '💖'; 
            heart.style.left = Math.random() * 95 + 'vw';
            heart.style.animationDuration = Math.random() * 2 + 3 + 's';
            heart.style.fontSize = Math.random() * 1.5 + 1.5 + 'em'; 
            document.body.appendChild(heart);
            setTimeout(() => {
                heart.remove();
            }, 5000); 
        }

        function renderStudents() {
            let htmlContent = '';
            
            students.forEach(student => {
                const imageClass = student.isShadow ? 'shadow-image' : 'student-image';
                
                // Hiển thị ảnh nhỏ (Dùng ảnh chính làm ảnh preview)
                const previewImagesHtml = `
                    <div class="preview-images">
                        <img src="${student.image}" alt="Ảnh ${student.name}" title="${student.name}">
                        </div>
                `;

                // Tạo Card chúc mừng
                htmlContent += `
                    <div class="student-card">
                        <h2>Gửi ${student.name}</h2>
                        <img src="${student.image}" alt="Ảnh ${student.name}" class="${imageClass}">
                        ${previewImagesHtml} 
                        <p class="congratulations">"${student.congratulation}"</p>
                        <p style="color: #ff6f61; font-weight: bold;">Chúc bạn 20/10 thật ý nghĩa! 🎉</p>
                    </div>
                `;
            });

            studentListDiv.innerHTML = htmlContent;
        }

        // Xử lý sự kiện khi bấm nút START
        startButton.addEventListener('click', () => {
            myAudio.play().catch(error => {
                console.log("Tự động phát nhạc bị chặn.");
            });

            welcomeScreen.style.opacity = '0';
            setTimeout(() => {
                welcomeScreen.style.display = 'none';
                mainContent.style.display = 'block';
                window.scrollTo(0, 0); 
            }, 1000);

            // Tạo hiệu ứng trái tim
            setInterval(createHeart, 250); 

            // Render nội dung
            renderStudents();
        });

    </script>
</body>
</html>
