<!DOCTYPE html>
<html>
<head>
<title>Dzikir Counter</title>

<style>

body{
font-family: Arial;
text-align:center;
background:#f1f37c;
}

.isi{
margin-top:80px;
background:rgb(5, 137, 65);
padding:30px;
width:300px;
margin-left:auto;
margin-right:auto;
border-radius:10px;
box-shadow:0 0 10px rgba(0,0,0,0.1);
}

#counter{
font-size:50px;
margin:20px;
}

input{
padding:8px;
width:80%;
margin-bottom:15px;
}

button{
padding:10px 15px;
margin:5px;
cursor:pointer;
}

button:active{
transform:scale(0.9);
}

#notif{
margin-top:15px;
color:rgb(233, 113, 223);
font-weight:bold;
}

</style>

</head>

<body>

<div class="isi">

<h2>Dzikir Harian</h2>

<h1 id="jumlah">0</h1>

<input type="number" id="target" placeholder="Masukkan Target">

<br>

<button onclick="tambah()">Tambah</button>
<button onclick="resetCounter()">Reset</button>

<p id="notif"></p>

</div>

<script>

let jumlahDzikir = 0;

function tambah(){

jumlahDzikir ++;

document.getElementById("jumlah").innerText = jumlahDzikir;

let targetDzikir = parseInt(document.getElementById("target").value);

if(!isNaN(targetDzikir)){

if(jumlahDzikir === targetDzikir){
document.getElementById("notif").innerText = "Alhamdulillah target tercapai!";
}

else if(jumlahDzikir > targetDzikir){
document.getElementById("notif").innerText = "Anda sudah Melewati Target";
}

}

}

function resetCounter(){

count = 0;

document.getElementById("isi").innerText = 0;

document.getElementById("notif").innerText = "";

}

</script>

</body>
</html>
