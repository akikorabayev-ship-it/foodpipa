<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<script src="https://telegram.org/js/telegram-web-app.js"></script>

<style>
body{
    font-family: Arial;
    padding:20px;
    text-align:center;
}

.item{
    padding:15px;
    margin:10px;
    background:#eee;
    border-radius:10px;
    cursor:pointer;
}
</style>
</head>

<body>

<h2>🍽 Выберите еду</h2>

<div class="item" onclick="select('Пицца')">🍕 Пицца</div>
<div class="item" onclick="select('Бургер')">🍔 Бургер</div>
<div class="item" onclick="select('Суши')">🍣 Суши</div>

<script>
const tg = window.Telegram.WebApp;
tg.expand();

function select(item){
    tg.sendData(item);
    tg.close();
}
</script>

</body>
</html>
