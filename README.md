<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hi, Mites 💜 | A Purple Date Invitation</title>
    <style>
        :root {
            --primary-purple: #8f5fd2;
            --light-purple: #f5eafe;
            --accent-lavender: #b39ddb;
            --dark-text: #44355b;
            --heart-pink: #ff90c2;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, var(--light-purple), #e4c6f5 90%);
            color: var(--dark-text);
            margin: 0;
            padding: 20px;
            min-height: 100vh;
            display: flex; 
            flex-direction: column; 
            align-items: center; 
            justify-content: center;
        }

        .invite-container {
            background: #fff;
            border-radius: 18px;
            box-shadow: 0 8px 24px rgba(143,95,210, 0.18);
            padding: 36px 26px 26px 26px;
            max-width: 450px;
            width: 100%;
            text-align: center;
            border: 3px solid var(--accent-lavender);
            box-sizing: border-box;
        }

        .heart {
            font-size: 2.3em;
            color: var(--heart-pink);
            animation: pulse 1.2s infinite;
        }
        @keyframes pulse {
            0%, 100% { transform: scale(1);}
            50% { transform: scale(1.18);}
        }

        h1 {
            margin: 0.3em 0 0.1em;
            color: var(--primary-purple);
            font-size: 2em;
        }

        .msg {
            background: var(--light-purple);
            border-left: 4px solid var(--primary-purple);
            padding: 15px;
            margin: 20px 0 26px 0;
            border-radius: 0 9px 9px 0;
            font-size: 0.95em;
            font-weight: 500;
            text-align: left;
            line-height: 1.6;
            max-height: 200px;
            overflow-y: auto;
        }

        .question {
            font-size: 1.2em;
            font-weight: bold;
            margin-bottom: 20px;
            color: var(--dark-text);
        }

        .btn-container {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
            position: relative;
            height: 50px;
        }

        .btn {
            padding: 12px 25px;
            font-size:
            padding: 0;
            min-height: 100vh;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
        }

        .invite-container {
            background: #fff;
            border-radius: 18px;
            box-shadow: 0 8px 24px rgba(143,95,210, 0.18);
            padding: 36px 26px 26px 26px;
            margin: 35px 0;
            max-width: 400px;
            width: 100%;
            text-align: center;
            border: 3px solid var(--accent-lavender);
            position: relative;
        }

        .heart {
            font-size: 2.3em;
            color: var(--heart-pink);
            animation: pulse 1.2s infinite;
        }
        @keyframes pulse {
            0%, 100% { transform: scale(1);}
            50% { transform: scale(1.18);}
        }

        h1 {
            margin: 0.3em 0 0.1em;
            color: var(--primary-purple);
            font-size: 2em;
        }
        .tiny-note {
            font-size: 11px;color: #9370b8;margin-top:13px;
        }
        .msg {
            background: var(--light-purple);
            border-left: 4px solid var(--primary-purple);
            padding: 15px;
            margin: 20px 0 26px 0;
            border-radius: 0 9px 9px 0;
            font-size: 1em;
            font-weight: 500;
            text-align: left;
        }
        .question {
            color: var(--primary-purple);
            font-weight: 700;
            font-size: 1.2em;
            margin-bottom: 24px;
        }
        .btns {
            display: flex;
            gap: 16px;
            justify-content: center;
            align-items: center;
        }
        .btn {
            padding: 11px 23px;
            font-size: 16px;
            font-weight: bold;
            border: none;
            border-radius: 24px;
            cursor: pointer;
            transition: all 0.2s;
        }
        #yesBtn {
            background: var(--primary-purple); color: white;
        }
        #yesBtn:hover { background:#723dbb;}
        #noBtn {
            background: #efecf6; color: #888;}
        #noBtn:hover {
            background: #f8c7e3; color:#E54;
        }

        /* Animated "No" button: */
        #noBtn {position:relative;}
        .calendar-section {
            margin:22px 0;
            display:none;
        }
        label {
            display: block; margin-bottom: 7px;
            font-weight:600; font-size:15px;color: var(--dark-text);
        }
        input[type="date"] {
            background:#faf6ff;
            border: 2px solid var(--accent-lavender);
            border-radius:8px;padding:10px;
            font-size:17px;color: var(--dark-text);
        }
        input[type="date"]:focus { border-color: var(--primary-purple);}
        #submitDateBtn {
            margin-top: 17px;
            background-color: var(--primary-purple);
            color: white;
            display: none;
        }
        .success-message {
            display: none;
            color: #54c374;
            font-weight: 600;
            margin-top: 19px;
            font-size: 1.07em;
        }
        .footer {
            font-size: 10.5px;
            color: #a194b2;
            margin-top: 28px;
        }
    </style>
</head>
<body>
    <div class="invite-container">
        <div class="heart">💜</div>
        <h1>For Mites</h1>
        <div class="tiny-note">the only girl I want to go out with</div>

        <div class="msg">
            Hi! Alam kong busy ka at gusto ko lang malaman kung pwede pa akong mag-ask ng date—purple lover & moon cat. Aalagaan mo sarili mo, ha? Sana bigyan mo pa ako ng chance na mapasaya ka. Kahit once (or thrice, or lagi) ulit.
        </div>
        
        <div id="mainQuestion" class="question">Are you available to go out? <span style="font-size:1.4em;">🥺💜</span></div>
        
        <div class="btns" id="actions">
            <button class="btn" id="yesBtn" onclick="acceptDate()">Yes</button>
            <button class="btn" id="noBtn" onmouseover="moveNoButton()" onclick="moveNoButton()">No</button>
        </div>

        <div class="calendar-section" id="calendarSection">
            <label for="datePicker">Pick a date (kahit tentative):</label>
            <input type="date" id="datePicker" onchange="showSubmitButton()">
            <br>
            <button class="btn" id="submitDateBtn" onclick="confirmDate()">Confirm</button>
        </div>
        <div class="success-message" id="successMessage"></div>
        <div class="footer">
            • Jan 5, 2026 • Choco Butternut • Sweet & Spicy Adobo • Purple & Moon 🐾
        </div>
    </div>
    <script>
        function moveNoButton() {
            const noBtn = document.getElementById('noBtn');
            const container = document.querySelector('.invite-container');
            const rect = container.getBoundingClientRect();
            const x = Math.random() * (window.innerWidth - 100);
            const y = Math.random() * (window.innerHeight - 50);

            noBtn.style.position = 'fixed';
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
        }
        function acceptDate() {
            document.getElementById('mainQuestion').innerHTML = "Yay! I can't wait to see you 🌸";
            document.getElementById('actions').style.display = 'none';
            document.getElementById('calendarSection').style.display = 'block';
        }
        function showSubmitButton() {
            document.getElementById('submitDateBtn').style.display = 'inline-block';
        }
        function confirmDate() {
            const chosenDate = document.getElementById('datePicker').value;
            if (!chosenDate) return;
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            const dateObject = new Date(chosenDate);
            const formattedDate = dateObject.toLocaleDateString('en-US', options);

            document.getElementById('calendarSection').style.display = 'none';
            const finalMsg = document.getElementById('successMessage');
            finalMsg.innerHTML = `YAY! ❤️ Marked <b>${formattedDate}</b> as our purple date. <br>Take a screenshot and send to me plss!`;
            finalMsg.style.display = 'block';
        }
    </script>
</body>
</html>            min-height: 100vh;
        }

        .container {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(125, 86, 165, 0.15);
            max-width: 500px;
            width: 100%;
            text-align: center;
            border: 2px solid var(--accent-lavender);
        }

        h1 {
            color: var(--primary-purple);
            font-size: 24px;
            margin-bottom: 10px;
        }

        .cat-animation {
            font-size: 50px;
            margin: 15px 0;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .letter-box {
            background: #FAF7FD;
            border-left: 4px solid var(--primary-purple);
            padding: 15px;
            text-align: left;
            font-size: 14px;
            line-height: 1.6;
            border-radius: 0 10px 10px 0;
            margin-bottom: 25px;
            max-height: 200px;
            overflow-y: auto;
        }

        .question {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 20px;
            color: var(--primary-purple);
        }

        /* Date Picker Styling */
        .calendar-section {
            margin: 20px 0;
            display: none; /* Hidden until they click Yes */
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            font-size: 14px;
        }

        input[type="date"] {
            padding: 10px;
            border: 2px solid var(--accent-lavender);
            border-radius: 8px;
            color: var(--dark-text);
            font-size: 16px;
            outline: none;
            width: 80%;
            max-width: 250px;
            text-align: center;
        }

        input[type="date"]:focus {
            border-color: var(--primary-purple);
        }

        /* Buttons */
        .btn-container {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
            position: relative;
            height: 50px;
        }

        .btn {
            padding: 12px 25px;
            font-size: 16px;
            font-weight: bold;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        #yesBtn {
            background-color: var(--primary-purple);
            color: white;
        }

        #yesBtn:hover {
            background-color: #6A4591;
            transform: scale(1.05);
        }

        #noBtn {
            background-color: #E0E0E0;
            color: #666;
            position: absolute;
            right: 80px;
        }

        #submitDateBtn {
            background-color: var(--primary-purple);
            color: white;
            margin-top: 15px;
            display: none;
        }

        .success-message {
            display: none;
            color: #4CAF50;
            font-weight: bold;
            margin-top: 15px;
            font-size: 16px;
        }

        .favorites-footer {
            font-size: 11px;
            color: #9A8CA7;
            margin-top: 30px;
            border-top: 1px dashed var(--accent-lavender);
            padding-top: 10px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Hi, Mites 💜</h1>
        <div class="cat-animation">🐈‍⬛✨</div>
        
        <div class="letter-box">
            Aalagaan mo sarili mo at wag mo papabayaan, mamahalin kita sa paraan na alam ko, mites. Sana hayaan mo ako na ipakita sayo yon at patunayan sayo lahat... Sayo at sayo ko lang ibibigay ang best version ko, mamahalin kita palagi kahit hindi ako ang kausap mo sa araw araw at ako ang unang papalakpak sa lahat ng achievement mo sa buhay. Maniniwala ako na tadhana ang gagawa ng paraan para sating dalawa, mahal na mahal kita Mikaela Prancine Pableo.
        </div>

        <div id="mainQuestion" class="question">Can I take you out on a date? ☕✨</div>

        <div class="btn-container" id="actions">
            <button class="btn" id="yesBtn" onclick="acceptDate()">Yes</button>
            <button class="btn" id="noBtn" onmouseover="moveNoButton()" onclick="moveNoButton()">No</button>
        </div>

        <!-- Hidden Calendar section until "Yes" is clicked -->
        <div class="calendar-section" id="calendarSection">
            <label for="datePicker">Pick a date that works best for you:</label>
            <input type="date" id="datePicker" onchange="showSubmitButton()">
            <br>
            <button class="btn" id="submitDateBtn" onclick="confirmDate()">Confirm Date 📅</button>
        </div>

        <div class="success-message" id="successMessage"></div>

        <div class="favorites-footer">
            January 5, 2026 • Choco Butternut • Yangnyeom No Garlic • Sweet & Spicy Adobo • Moon 🐾
        </div>
    </div>

    <script>
        function moveNoButton() {
            const noBtn = document.getElementById('noBtn');
            // Generate random movement positions within bounds
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth - 40);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight - 40);
            
            // Move button outside the container absolute bounds safely
            noBtn.style.position = 'fixed';
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
        }

        function acceptDate() {
            document.getElementById('mainQuestion').innerHTML = "Yay! I can't wait to see you. 🥰";
            document.getElementById('actions').style.display = 'none';
            document.getElementById('calendarSection').style.display = 'block';
        }

        function showSubmitButton() {
            document.getElementById('submitDateBtn').style.display = 'inline-block';
        }

        function confirmDate() {
            const chosenDate = document.getElementById('datePicker').value;
            
            // Format the date beautifully
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            const dateObject = new Date(chosenDate);
            const formattedDate = dateObject.toLocaleDateString('en-US', options);

            document.getElementById('calendarSection').style.display = 'none';
            
            const finalMsg = document.getElementById('successMessage');
            finalMsg.innerHTML = `Perfect! Marked for ${formattedDate} 💜<br><br>Take a screenshot of this and send it to me!`;
            finalMsg.style.display = 'block';
        }
    </script>
</body>
</html>
