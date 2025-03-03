<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun!</title>
    <style>
        body {
            text-align: center;
            background-color: #87CEEB;
            font-family: Arial, sans-serif;
        }
        .container {
            margin-top: 50px;
        }
        .balloon {
            position: absolute;
            width: 50px;
            height: 70px;
            background: red;
            border-radius: 50%;
            animation: float 5s ease-in-out infinite;
        }
        @keyframes float {
            0% { transform: translateY(100vh); opacity: 1; }
            100% { transform: translateY(-10vh); opacity: 0; }
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            margin-top: 20px;
            background-color: #FF69B4;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #FF1493;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🎉 Selamat Ulang Tahun! 🎂</h1>
        <p>Semoga harimu menyenangkan dan penuh kebahagiaan!</p>
        <button onclick="tampilkanPesan()">Klik untuk Kejutan!</button>
    </div>
    
    <script>
        function tampilkanPesan() {
            alert("Selamat Ulang Tahun! Semoga semua impianmu menjadi kenyataan!");
        }
        
        function buatBalon() {
            let balon = document.createElement("div");
            balon.classList.add("balloon");
            document.body.appendChild(balon);
            
            let warna = ["red", "blue", "yellow", "green", "purple", "orange"];
            balon.style.background = warna[Math.floor(Math.random() * warna.length)];
            balon.style.left = Math.random() * 100 + "vw";
            
            setTimeout(() => {
                balon.remove();
            }, 5000);
        }
        
        setInterval(buatBalon, 500);
    </script>
</body>
</html>
