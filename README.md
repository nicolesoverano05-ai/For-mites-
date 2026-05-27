# For-mites-
Sincere love for her
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Mites 💜</title>
    <style>
        :root {
            --primary-purple: #7D56A5;
            --light-purple: #F3EAFB;
            --accent-lavender: #B39DDB;
            --dark-text: #4A3E56;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light-purple);
            color: var(--dark-text);
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
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
