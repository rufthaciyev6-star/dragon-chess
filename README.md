<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Dragon Chess</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;
 background:#17191f;
 color:white;
 font-family:Arial,sans-serif;
 display:flex;
 justify-content:center;
 align-items:center;
 min-height:100vh;
}
.game{
 width:min(95vw,900px);
 text-align:center;
}
h1{margin:10px}
#status{margin:10px;font-size:18px}
.board{
 width:min(92vw,720px);
 aspect-ratio:1;
 margin:auto;
 display:grid;
 grid-template-columns:repeat(8,1fr);
 border:4px solid #111;
}
.square{
 display:flex;
 justify-content:center;
 align-items:center;
 font-size:clamp(30px,8vw,68px);
 cursor:pointer;
 user-select:none;
}
.light{background:#f0d9b5}
.dark{background:#b58863}
.selected{outline:5px solid #ffd43b;outline-offset:-5px}
.possible{box-shadow:inset 0 0 0 5px #65d46e}
button{
 margin:12px 5px;
 padding:12px 20px;
 border:0;
 border-radius:10px;
 cursor:pointer;
 font-size:16px;
}
</style>
</head>

<body>

<div class="game">
<h1>♟ Dragon Chess ♟</h1>
<div id="status">Ağların növbəsi</div>

<div id="board" class="board"></div>

<button onclick="newGame()">Yeni oyun
