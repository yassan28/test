<!DOCTYPE html>
<html>
<head>
<meta charset="Shift_JIS">
<title>じゃんけんゲーム</title>
</head>
<body>
<div id="message1" style="position:absolute; left:10px; top:10px">
相手の選択は ？
</div>
<div id="message2" style="position:absolute; left:10px; top:40px">
勝敗の結果は ？
</div>
<form style="position:absolute; left:10px; top:70px">
あなたの選択は　
<select id="mySelect">
<option>グー</option>
<option>チョキ</option>
<option>パー</option>
</select>
<input type="button" value="決定" onclick="myGame()">
</form>

<script>
function myGame(){
myNumber = document.getElementById("mySelect").selectedIndex;
hisNumber = Math.floor(Math.random()*3);
if( hisNumber == 0 ){
hisHand = "グー";
}
if( hisNumber == 1 ){
hisHand = "チョキ";
}
if( hisNumber == 2 ){
hisHand = "パー";
}
if( myNumber - hisNumber == -2 ){
judge = "あなたの 負け";
}
if( myNumber - hisNumber == -1 ){
judge = "あなたの 勝ち";
}
if( myNumber - hisNumber == 0 ){
judge = "両者の 引き分け";
}
if( myNumber - hisNumber == 1 ){
judge = "あなたの 負け";
}
if( myNumber - hisNumber == 2 ){
judge = "あなたの 勝ち";
}
document.getElementById("message1").innerHTML = "相手の選択は "+hisHand;
document.getElementById("message2").innerHTML = "勝敗の結果は "+judge;
}
</script>

</body>
</html> 
