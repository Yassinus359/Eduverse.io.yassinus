<!-- ========================= -->
<!-- INDEX.HTML (WITH QUIZ + EXERCISES) -->
<!-- ========================= -->
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Eduverse - Plateforme Éducative</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Poppins', sans-serif; }
    body { background: #0f172a; color: white; }

    header { display: flex; justify-content: space-between; padding: 20px 40px; background: #020617; }
    header h1 { color: #38bdf8; }

    nav a { color: white; margin-left: 20px; text-decoration: none; }
    nav a:hover { color: #38bdf8; }

    .hero { text-align: center; padding: 80px 20px; }

    .features { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px,1fr)); gap: 20px; padding: 40px; }

    .card { background: #020617; padding: 20px; border-radius: 15px; }

    .quiz { padding: 40px; }

    .question { margin-bottom: 20px; }

    button {
      padding: 10px 20px; margin-top: 10px;
      background: #38bdf8; border: none; border-radius: 10px;
      cursor: pointer;
    }

    footer { text-align: center; padding: 20px; background: #020617; }
  </style>
</head>
<body>

<header>
  <h1>Eduverse</h1>
  <nav>
    <a href="#">Accueil</a>
    <a href="#quiz">Quiz</a>
  </nav>
</header>

<section class="hero">
  <h2>Bienvenue sur Eduverse 🚀</h2>
  <p>Teste tes connaissances avec des quiz interactifs !</p>
</section>

<section class="features">
  <div class="card">
    <h3>📚 Exercice 1</h3>
    <p>Combien font 5 + 3 ?</p>
    <button onclick="checkAnswer(8)">Voir réponse</button>
  </div>

  <div class="card">
    <h3>📚 Exercice 2</h3>
    <p>Quelle est la capitale de la France ?</p>
    <button onclick="alert('Paris')">Voir réponse</button>
  </div>
</section>

<section class="quiz" id="quiz">
  <h2>📝 Quiz</h2>

  <div class="question">
    <p>1. Combien font 2 × 3 ?</p>
    <button onclick="answerQuiz(this, true)">6</button>
    <button onclick="answerQuiz(this, false)">5</button>
  </div>

  <div class="question">
    <p>2. Le soleil est une ?</p>
    <button onclick="answerQuiz(this, true)">Étoile</button>
    <button onclick="answerQuiz(this, false)">Planète</button>
  </div>

  <p id="result"></p>
</section>

<footer>
  <p>© 2026 Eduverse</p>
</footer>

<script>
let score = 0;

function checkAnswer(correct) {
  let user = prompt("Ta réponse ?");
  if (parseInt(user) === correct) {
    alert("Bonne réponse !");
  } else {
    alert("Faux ! La bonne réponse est " + correct);
  }
}

function answerQuiz(btn, isCorrect) {
  if (isCorrect) {
    score++;
    btn.style.background = "green";
  } else {
    btn.style.background = "red";
  }

  document.getElementById("result").innerText = "Score: " + score;
}
</script>

</body>
</html>


<!-- ========================= -->
<!-- README.md -->
<!-- ========================= -->

# 🚀 Eduverse

Plateforme éducative avec exercices et quiz interactifs.

## ✨ Fonctionnalités
- 📚 Exercices simples
- 📝 Quiz interactifs avec score
- 💻 Interface moderne

## 🛠️ Technologies
- HTML
- CSS
- JavaScript

## 👨‍💻 Auteur
Yassine

---

🔥 Projet en évolution !
