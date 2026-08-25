<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PressEarn Tool</title>
</head>

<body>
  <h1>PressEarn Tool</h1>
  <p>Your link distribution dashboard</p>

  <input
    type="url"
    id="articleLink"
    placeholder="Paste your approved article link"
  >

  <button onclick="addLink()">Add Article</button>

  <h2>My Articles</h2>
  <div id="articles"></div>

  <script>
    function addLink() {
      const link = document.getElementById("articleLink").value.trim();

      if (!link) {
        alert("Please enter an article link.");
        return;
      }

      const article = document.createElement("p");

      article.innerHTML =
        `<a href="${link}" target="_blank">${link}</a>`;

      document.getElementById("articles").appendChild(article);

      document.getElementById("articleLink").value = "";
    }
  </script>
</body>
</html>
