<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Cutuu ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:Arial, sans-serif;
    background:linear-gradient(135deg,#ff9a9e,#fad0c4);
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    overflow:hidden;
}

.container{
    max-width:800px;
    padding:30px;
    color:white;
}

h1{
    font-size:3rem;
    margin-bottom:20px;
}

p{
    font-size:1.2rem;
    line-height:1.8;
    margin-bottom:15px;
}

.heart{
    font-size:60px;
    animation:beat 1s infinite;
}

@keyframes beat{
    0%,100%{transform:scale(1);}
    50%{transform:scale(1.2);}
}

.btn{
    margin-top:20px;
    padding:15px 35px;
    border:none;
    border-radius:50px;
    background:white;
    color:#ff4d6d;
    font-size:1.1rem;
    cursor:pointer;
    transition:0.3s;
}

.btn:hover{
    transform:scale(1.08);
}

.popup{
    display:none;
    position:fixed;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    background:white;
    color:#ff4d6d;
    padding:30px;
    border-radius:20px;
    width:90%;
    max-width:500px;
    box-shadow:0 10px 30px rgba(0,0,0,0.3);
    z-index:999;
    animation:pop 0.4s ease;
}

@keyframes pop{
    from{
        transform:translate(-50%,-50%) scale(0.5);
        opacity:0;
    }
    to{
        transform:translate(-50%,-50%) scale(1);
        opacity:1;
    }
}

.close{
    margin-top:15px;
    padding:10px 25px;
    border:none;
    border-radius:30px;
    background:#ff4d6d;
    color:white;
    cursor:pointer;
}

.floating-heart{
    position:absolute;
    color:white;
    animation:float 8s linear infinite;
}

@keyframes float{
    from{
        transform:translateY(100vh);
        opacity:1;
    }
    to{
        transform:translateY(-100px);
        opacity:0;
    }
}
</style>
</head>

<body>

<div class="container">

    <div class="heart">❤️</div>

    <h1>I'm Sorry, Cutuu ❤️</h1>

    <p>
        I know I messed up and hurt you, and I'm truly sorry.
    </p>

    <p>
        You are the best thing that has ever happened to me.
        Every happy moment in my life feels brighter because of you.
    </p>

    <p>
        I know apologies mean little without actions, so I promise to keep
        improving myself and becoming a better person every single day.
    </p>

    <p>
        No matter what, I'll never stop appreciating how special you are to me.
    </p>

    <button class="btn" onclick="openPopup()">
        Click Here ❤️
    </button>

</div>

<div class="popup" id="popup">

    <h2>🥺 Dear Cutuu ❤️</h2>

    <p>
        Thank you for being patient with me even when I don't deserve it.
    </p>

    <p>
        You are my favorite person, my comfort, my happiness,
        and the most beautiful part of my life.
    </p>

    <p>
        I promise I will keep trying, keep learning,
        and keep becoming better for you every day.
    </p>

    <p>
        I love you, Cutuu ❤️
    </p>

    <button class="close" onclick="closePopup()">
        Aww ❤️
    </button>

</div>

<script>

function openPopup(){
    document.getElementById("popup").style.display="block";
}

function closePopup(){
    document.getElementById("popup").style.display="none";
}

function createHeart(){
    const heart=document.createElement("div");
    heart.classList.add("floating-heart");
    heart.innerHTML="❤️";

    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(Math.random()*20+20)+"px";

    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },8000);
}

setInterval(createHeart,500);

</script>

</body>
</html>
