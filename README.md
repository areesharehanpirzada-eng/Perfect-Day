<!DOCTYPE html>
<html>

<head>
<title>My Perfect Day</title>

<style>

body {
    font-family: Forte;
    text-align: center;
    background-color: lightblue;
    padding: 30px;
     }

.box {
    background-color: beige;
    width: 70%;
    margin: auto;
    padding: 25px;
    border-radius: 20px;
     }

button {
    padding: 12px;
    margin: 7px;
    border: none;
    border-radius: 10px;
    background-color: #ffd166;
    cursor: pointer;
       }

button:hover {
    background-color: orange;
             }
 
#result {
    display: none;
    margin-top: 25px;
        }

</style>
</head>


<body>

<div class="box">

<h1>☀️ MY PERFECT DAY ☀️</h1>

<p>Answer a few questions and let's find your perfect day score!</p>


<h2 id="question">Where would you spend your perfect day?</h2>


<div id="buttons">

<button onclick="choose(1)">🏖️ Beach</button>

<button onclick="choose(2)">🏔️ Mountains</button>

<button onclick="choose(3)">🏠 At Home</button>

<button onclick="choose(4)">🏙️ City</button>

</div>


<div id="result">

<h2>✨ YOUR RESULT ✨</h2>

<p id="answer"></p>

<p id="score"></p>

</div>



<script>

var score = 0;
var question = 1;


function choose(choice) {

    if (choice == 1) {
        score = score + 5;
                     }

    if (choice == 2) {
        score = score + 4;
                     }

    if (choice == 3) {
        score = score + 2;
                     }

    if (choice == 4) {
        score = score + 3;
                     }
 

    question = question + 1;


    if (question == 2) {

        document.getElementById("question").innerHTML =
        "Who would you spend your perfect day with?";

        document.getElementById("buttons").innerHTML =

        '<button onclick="choose(2)">👯 Friends</button>' +
        '<button onclick="choose(3)">👨‍👩‍👧 Family</button>' +
        '<button onclick="choose(1)">🧍 Myself</button>' +
        '<button onclick="choose(4)">🌎 New People</button>';

    }


    else if (question == 3) {

        document.getElementById("question").innerHTML =
        "What would you love to do?";

        document.getElementById("buttons").innerHTML =

        '<button onclick="choose(4)">🏐 Play Sports</button>' +
        '<button onclick="choose(2)">🎮 Gaming</button>' +
        '<button onclick="choose(1)">📚 Reading</button>' +
        '<button onclick="choose(3)">🎨 Go to rides</button>';

    }


    else if (question == 4) {

        document.getElementById("question").innerHTML =
        "Pick your perfect food!";

        document.getElementById("buttons").innerHTML =

        '<button onclick="choose(3)">🍕 Pizza</button>' +
        '<button onclick="choose(2)">🍜 Noodles</button>' +
        '<button onclick="choose(4)">🍦 Ice Cream</button>' +
        '<button onclick="choose(1)">🍔 Burger</button>';

    }


    else if (question == 5) {

        document.getElementById("question").innerHTML =
        "How would you end your day?";

        document.getElementById("buttons").innerHTML =

        '<button onclick="choose(4)">🌅 Sunset</button>' +
        '<button onclick="choose(2)">🎬 Movie</button>' +
        '<button onclick="choose(3)">🎧 Music</button>' +
        '<button onclick="choose(1)">🌌 Stargazing</button>';

    }


    else {

        showResult();

    }

}


function showResult() {

    document.getElementById("buttons").style.display = "none";

    document.getElementById("question").style.display = "none";

    document.getElementById("result").style.display = "block";


    document.getElementById("score").innerHTML =
    "Your Perfect Day Score is " + score + " / 20";


    if (score >= 18) {

        document.getElementById("answer").innerHTML =
        "🌟 You are an ADVENTURER!<br><br>" +
        "Your perfect day is full of fun, friends and exciting experiences!";

    }

    else if (score >= 15) {

        document.getElementById("answer").innerHTML =
        "✨ You are a HAPPY SOUL!<br><br>" +
        "Your perfect day is all about enjoying the little things.";

    }

    else {

        document.getElementById("answer").innerHTML =
        "🌿 You are a PEACE SEEKER!<br><br>" +
        "Your perfect day is calm, relaxing and stress-free.";

    }

}

</script>

</body>

</html>
