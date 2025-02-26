<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our Perfect Date 💖</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #fff0f5;
            color: #333;
            text-align: center;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            background: linear-gradient(135deg, #ffebee, #ffc1e3);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        h1 {
            color: #e91e63;
            font-size: 2.5em;
            margin-bottom: 10px;
            animation: heartbeat 1.5s infinite;
        }

        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
        }

        p {
            font-size: 1.2em;
            margin-bottom: 20px;
            color: #555;
        }

        label {
            display: block;
            margin: 15px 0 5px;
            font-weight: bold;
            color: #d81b60;
        }

        select, button, input[type="date"] {
            width: 100%;
            padding: 12px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }

        button {
            background-color: #e91e63;
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        button:hover {
            background-color: #d81b60;
            transform: scale(1.05);
        }

        #result {
            margin-top: 20px;
            font-size: 1.2em;
            color: #444;
            line-height: 1.6;
            animation: fadeIn 1s ease;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        .heart {
            font-size: 2em;
            color: #e91e63;
            margin-top: 10px;
            animation: heartbeat 1.5s infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Will You Be My Valentine, Jinx? 💖</h1>
        <p>You’re special to me, and I want our day to be unforgettable. Please choose how we’ll spend it together!</p>
        <form id="dateForm">
            <label for="food">What do you want to eat? 🍽️</label>
            <select id="food" required>
                <option value="" disabled selected>Select an option</option>
                <option value="Jollibee">Jollibee</option>
                <option value="Samgyup">Samgyup</option>
                <option value="Mcdo">Inasal</option>
                <option value="Street Foods">Street Foods</option>
            </select>
            
            <label for="place">Where do you want to go? 🌍</label>
            <select id="place" required>
                <option value="" disabled selected>Select an option</option>
                <option value="Tagaytay">Tagaytay</option>
                <option value="Somewhere quite & piece">Somewhere quite & piece</option>
                <option value="SM">SM</option>
                <option value="Park">Park</option>
            </select>
            
            <label for="movie">Which movie do you want to watch? 🎬</label>
            <select id="movie" required>
                <option value="" disabled selected>Select an option</option>
                <option value="SM Cinema">SM Cinema</option>
                <option value="Netflix">Netflix</option>
                <option value="Kdrama">Kdrama</option>
                <option value="Horror">Horror</option>
            </select>

            <label for="date">When should we go on our date? 📅</label>
            <input type="date" id="date" required>
            
            <button type="submit">Plan Our Date ❤️</button>
             <a href="index.html"><button type="">next</button></a>
        </form>
        <div id="result"></div>
    </div>

    <script>
        document.getElementById("dateForm").addEventListener("submit", function (event) {
            event.preventDefault();

            const food = document.getElementById("food").value;
            const place = document.getElementById("place").value;
            const movie = document.getElementById("movie").value;
            const date = document.getElementById("date").value;

            const resultDiv = document.getElementById("result");
            if (date) {
                resultDiv.innerHTML = `
                    <p>Thank you for sharing your choices, Jinx! Here’s our plan:</p>
                    <ul>
                        <li>We’ll enjoy some delicious <strong>${food}</strong>.</li>
                        <li>Then, we’ll spend quality time at <strong>${place}</strong>.</li>
                        <li>Finally, we’ll watch a <strong>${movie}</strong> movie together.</li>
                        <li>All of this will happen on <strong>${new Date(date).toDateString()}</strong>.</li>
                    </ul>
                    <p>I’m really looking forward to this magical day with you! 💕</p>
                    <div class="heart">❤️</div>
                `;
            } else {
                resultDiv.innerHTML = `<p>Please select a date for our date! ❤️</p>`;
            }
        });
    </script>
</body>
</html>

