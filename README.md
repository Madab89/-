<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ইসলামিক কুইজ</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            padding: 20px;
        }
        .quiz-container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 500px;
            margin: auto;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .correct {
            background-color: #28a745;
            color: white;
        }
        .wrong {
            background-color: #dc3545;
            color: white;
        }
        #result {
            font-size: 18px;
            margin-top: 15px;
        }
    </style>
</head>
<body>
    <div class="quiz-container">
        <h2>ইসলামিক কুইজ</h2>
        <p>কুরআনের সবচেয়ে ছোট সূরার নাম কী?</p>
        <button onclick="checkAnswer(this, true)">সূরা কাভসার</button>
        <button onclick="checkAnswer(this, false)">সূরা ফাতিহা</button>
        <button onclick="checkAnswer(this, false)">সূরা ইখলাস</button>
        <p id="result"></p>
    </div>

    <script>
        function checkAnswer(button, isCorrect) {
            let buttons = document.querySelectorAll("button");
            buttons.forEach(btn => btn.disabled = true); 
            
            if (isCorrect) {
                button.classList.add("correct");
                document.getElementById("result").innerHTML = "✅ সঠিক উত্তর! সূরা কাভসার হলো কুরআনের সবচেয়ে ছোট সূরা।";
            } else {
                button.classList.add("wrong");
                document.getElementById("result").innerHTML = "❌ ভুল উত্তর! আবার চেষ্টা করুন।";
            }
        }
    </script>
</body>
</html>
