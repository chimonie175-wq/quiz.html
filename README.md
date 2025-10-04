# quiz.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dare to Be Different - Bible Quiz</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background: #f9f9f9;
      color: #333;
    }
    h1 {
      text-align: center;
      color: #2a4d7d;
    }
    .quiz-container {
      max-width: 900px;
      margin: auto;
      background: #fff;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .question {
      margin-bottom: 25px;
      padding: 15px;
      border-bottom: 1px solid #ddd;
    }
    .question h3 {
      margin-bottom: 10px;
      color: #2a4d7d;
    }
    input[type="text"], textarea {
      width: 100%;
      padding: 8px;
      margin-top: 6px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      margin-top: 10px;
      background: #2a4d7d;
      color: white;
      border: none;
      padding: 8px 16px;
      font-size: 14px;
      border-radius: 6px;
      cursor: pointer;
    }
    button:hover {
      background: #1d355e;
    }
    .result {
      margin-top: 8px;
      font-weight: bold;
    }
    .correct {
      color: green;
    }
    .wrong {
      color: red;
    }
    #finalScore {
      text-align: center;
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="quiz-container">
    <h1>Dare to Be Different - Bible Quiz</h1>
    <form id="quizForm">

      <!-- Example Question Format -->
      <div class="question" id="q1-block">
        <h3>1. How many bulbs were in the first slide, and who does the only bulb with light represent?</h3>
        <input type="text" name="q1">
        <button type="button" onclick="checkSingle('q1')">Check</button>
        <div class="result" id="q1-result"></div>
      </div>

      <div class="question" id="q2-block">
        <h3>2. Recite the memory verse (Romans 12:2)</h3>
        <textarea name="q2"></textarea>
        <button type="button" onclick="checkSingle('q2')">Check</button>
        <div class="result" id="q2-result"></div>
      </div>

      <!-- Repeat for all 20 -->
      <div class="question" id="q3-block"><h3>3. What does it mean to be different?</h3><textarea name="q3"></textarea><button type="button" onclick="checkSingle('q3')">Check</button><div id="q3-result" class="result"></div></div>
      <div class="question" id="q4-block"><h3>4. When we say the world is filled with darkness, what do we mean?</h3><textarea name="q4"></textarea><button type="button" onclick="checkSingle('q4')">Check</button><div id="q4-result" class="result"></div></div>
      <div class="question" id="q5-block"><h3>5. Even in a bad world, what does God expect his children to do?</h3><textarea name="q5"></textarea><button type="button" onclick="checkSingle('q5')">Check</button><div id="q5-result" class="result"></div></div>
      <div class="question" id="q6-block"><h3>6. Wherever you find yourself you must be bold to stand for __________</h3><input type="text" name="q6"><button type="button" onclick="checkSingle('q6')">Check</button><div id="q6-result" class="result"></div></div>
      <div class="question" id="q7-block"><h3>7. God is also _____________ according to 1 John 1:7</h3><label><input type="radio" name="q7" value="a"> Friend</label><br><label><input type="radio" name="q7" value="b"> Light</label><br><label><input type="radio" name="q7" value="c"> Father</label><br><button type="button" onclick="checkSingle('q7')">Check</button><div id="q7-result" class="result"></div></div>
      <div class="question" id="q8-block"><h3>8. Sin means _____________</h3><input type="text" name="q8"><button type="button" onclick="checkSingle('q8')">Check</button><div id="q8-result" class="result"></div></div>
      <div class="question" id="q9-block"><h3>9. Complete: In 1 Peter 1:16 We must be ___________ because he is _____________</h3><input type="text" name="q9"><button type="button" onclick="checkSingle('q9')">Check</button><div id="q9-result" class="result"></div></div>
      <div class="question" id="q10-block"><h3>10. Mention 3 people in the Bible that were different and stood for righteousness</h3><textarea name="q10"></textarea><button type="button" onclick="checkSingle('q10')">Check</button><div id="q10-result" class="result"></div></div>
      <div class="question" id="q11-block"><h3>11. As children of God who is our role model?</h3><input type="text" name="q11"><button type="button" onclick="checkSingle('q11')">Check</button><div id="q11-result" class="result"></div></div>
      <div class="question" id="q12-block"><h3>12. God still expects us to live pure and holy lives.</h3><label><input type="radio" name="q12" value="true"> True</label><br><label><input type="radio" name="q12" value="false"> False</label><br><button type="button" onclick="checkSingle('q12')">Check</button><div id="q12-result" class="result"></div></div>
      <div class="question" id="q13-block"><h3>13. We are the _________ of the world</h3><label><input type="radio" name="q13" value="a"> People</label><br><label><input type="radio" name="q13" value="b"> Light</label><br><label><input type="radio" name="q13" value="c"> Ambassador</label><br><button type="button" onclick="checkSingle('q13')">Check</button><div id="q13-result" class="result"></div></div>
      <div class="question" id="q14-block"><h3>14. Daniel refused to defile himself with ________</h3><input type="text" name="q14"><button type="button" onclick="checkSingle('q14')">Check</button><div id="q14-result" class="result"></div></div>
      <div class="question" id="q15-block"><h3>15. We must stand for Christ _________</h3><label><input type="radio" name="q15" value="a"> Just at home</label><br><label><input type="radio" name="q15" value="b"> Only some places</label><br><label><input type="radio" name="q15" value="c"> Anywhere we find ourselves</label><br><button type="button" onclick="checkSingle('q15')">Check</button><div id="q15-result" class="result"></div></div>
      <div class="question" id="q16-block"><h3>16. You must choose and decide to stand for Christ.</h3><label><input type="radio" name="q16" value="true"> True</label><br><label><input type="radio" name="q16" value="false"> False</label><br><button type="button" onclick="checkSingle('q16')">Check</button><div id="q16-result" class="result"></div></div>
      <div class="question" id="q17-block"><h3>17. How was Noah different and what did God ask him to do?</h3><textarea name="q17"></textarea><button type="button" onclick="checkSingle('q17')">Check</button><div id="q17-result" class="result"></div></div>
      <div class="question" id="q18-block"><h3>18. To be set apart for God means to be ?</h3><label><input type="radio" name="q18" value="a"> To be used by God</label><br><label><input type="radio" name="q18" value="b"> To follow others</label><br><label><input type="radio" name="q18" value="c"> To do what you want</label><br><button type="button" onclick="checkSingle('q18')">Check</button><div id="q18-result" class="result"></div></div>
      <div class="question" id="q19-block"><h3>19. What were the names of the 3 Hebrew boys that were thrown into the fire?</h3><input type="text" name="q19"><button type="button" onclick="checkSingle('q19')">Check</button><div id="q19-result" class="result"></div></div>
      <div class="question" id="q20-block"><h3>20. Give 2 lessons you learnt from the topic "Dare to be Different"</h3><textarea name="q20"></textarea><button type="button" onclick="checkSingle('q20')">Check</button><div id="q20-result" class="result"></div></div>

      <button type="button" onclick="showFinalScore()">Finish Quiz</button>
    </form>

    <div id="finalScore"></div>
  </div>

<script>
 // Correct answers
  let answers = {
    q1: "1 bulb - Jesus",
    q2: "do not conform",
    q3: "holy",
    q4: "sin",
    q5: "shine",
    q6: "christ",
    q7: "b",
    q8: "disobedience",
    q9: "holy",
    q10: "daniel joseph esther",
    q11: "jesus",
    q12: "true",
    q13: "b",
    q14: "king",
    q15: "c",
    q16: "true",
    q17: "ark",
    q18: "a",
    q19: "shadrach meshach abednego",
    q20: "open"
  };

  let score = 0;
  let attempted = {};

  function checkSingle(q) {
    let form = document.forms['quizForm'];
    let userAnswer = "";

    if (form[q].type === "radio" || (form[q].length && form[q][0].type === "radio")) {
      let radios = form[q];
      for (let r of radios) {
        if (r.checked) userAnswer = r.value;
      }
    } else {
      userAnswer = form[q].value.trim().toLowerCase();
    }

    let resultDiv = document.getElementById(q+"-result");
    resultDiv.innerHTML = "";

    if (!userAnswer) {
      resultDiv.innerHTML = "⚠ Please enter an answer!";
      return;
    }

    if (answers[q] === "open") {
      resultDiv.innerHTML = "✅ Open-ended, answer may vary.";
      if (!attempted[q]) score++;
    } else if (answers[q].includes(userAnswer)) {
      resultDiv.innerHTML = "<span class='correct'>✅ Correct</span>";
      if (!attempted[q]) score++;
    } else {
      resultDiv.innerHTML = `<span class='wrong'>❌ Wrong.</span> Correct answer: ${answers[q]}`;
    }

    attempted[q] = true;
  }

  function showFinalScore() {
    document.getElementById("finalScore").innerHTML = 
      "Your Score: " + score + " / 20";
  }
</script>

</body>
</html>
