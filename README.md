<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Local Singles Near You</title>

<meta name="description" content="Meet local singles near you and start chatting instantly.">

<meta name="robots" content="index,follow">

<style>

body{
margin:0;
font-family:Arial;
background:#030712;
color:white;
text-align:center;
}

.container{
width:95%;
max-width:420px;
margin:auto;
padding-top:30px;
}

h1{
font-size:26px;
}

.profile{
background:#1f2937;
padding:15px;
border-radius:15px;
margin-bottom:15px;
}

.profile img{
width:100%;
border-radius:12px;
}

.profile h3{
margin:8px 0;
}

.btn{
display:block;
background:#ec4899;
padding:14px;
border-radius:10px;
text-decoration:none;
color:white;
font-size:18px;
font-weight:bold;
margin-top:10px;
}

.enter-btn{
background:#22c55e;
padding:14px;
border-radius:10px;
color:white;
font-size:18px;
cursor:pointer;
display:inline-block;
margin-top:10px;
}

.age-gate{
background:#111827;
padding:25px;
border-radius:15px;
}

.progress{
background:#374151;
height:10px;
border-radius:8px;
margin-top:8px;
}

.bar{
background:#22c55e;
height:10px;
width:78%;
border-radius:8px;
}

footer{
margin-top:40px;
font-size:12px;
color:#9ca3af;
}

footer a{
color:#9ca3af;
text-decoration:none;
margin:0 5px;
}

.sticky{
position:fixed;
bottom:0;
left:0;
width:100%;
background:#ec4899;
padding:15px;
}

</style>

</head>

<body>

<div class="container">

<div id="ageGate" class="age-gate">

<h1>🔞 Age Verification</h1>

<p>You must be 18+ to continue.</p>

<a class="enter-btn" onclick="step1()">Enter Site</a>

</div>


<div id="step1" style="display:none">

<h2>Select Your Gender</h2>

<button onclick="step2()" class="enter-btn">Male</button>
<button onclick="step2()" class="enter-btn">Female</button>

</div>


<div id="step2" style="display:none">

<h2>Profiles Available Near You</h2>

<p id="countdown" style="color:#fbbf24">
Offer expires in: 04:59
</p>

<div class="progress">
<div class="bar"></div>
</div>

<p style="font-size:13px;color:#9ca3af">
78% of profiles matched in your area
</p>

<br>

<div class="profile">

<img src="https://images.unsplash.com/photo-1607746882042-944635dfe10e?auto=format&w=400&q=80">

<h3>Jessica, 24</h3>

<a href="YOUR_CPA_LINK" class="btn" target="_blank">
Start Chat
</a>

</div>


<div class="profile">

<img src="https://images.unsplash.com/photo-1614287421678-76c1d2d0e4e6?auto=format&w=400&q=80">

<h3>Amanda, 27</h3>

<a href="YOUR_CPA_LINK" class="btn" target="_blank">
Send Message
</a>

</div>


<div class="profile">

<img src="https://images.unsplash.com/photo-1614285518395-8b8e37f1c22e?auto=format&w=400&q=80">

<h3>Sophia, 22</h3>

<a href="YOUR_CPA_LINK" class="btn" target="_blank">
View Profile
</a>

</div>

</div>

<footer>

<a href="privacy.html">Privacy</a> |
<a href="terms.html">Terms</a> |
<a href="contact.html">Contact</a>

</footer>

</div>

<div class="sticky">

<a href="YOUR_CPA_LINK"
style="color:white;font-size:18px;font-weight:bold;text-decoration:none">
Start Chatting Now
</a>

</div>


<script>

function step1(){

document.getElementById("ageGate").style.display="none";
document.getElementById("step1").style.display="block";

}

function step2(){

document.getElementById("step1").style.display="none";
document.getElementById("step2").style.display="block";

}

var time=299;

setInterval(function(){

var minutes=Math.floor(time/60);
var seconds=time%60;

document.getElementById("countdown").innerHTML=
"Offer expires in: "+minutes+":"+(seconds<10?"0":"")+seconds;

time--;

if(time<=0){
time=299;
}

},1000);

</script>

</body>
</html>
