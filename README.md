<!DOCTYPE html>
<html lang="no">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vik fra meg</title>
    <style>
      div {
    border-radius: 50%;
}

.ring {
    width: 200px;
    height: 200px;
    /* background-color: rgb(255, 150, 150); */
}

.prikk {
    width: 70px;
    height: 70px;
    background-color: black;
    transform: translate(100%,100%);
}
    </style>
</head>

<body>
    <script>
      var bodyEl = document.querySelector("body");
var ringEl = document.createElement("div");
var prikkEl = document.createElement("div");
var bredde = window.innerWidth;
var hoyde = window.innerHeight;


ringEl.addEventListener("mouseover", forsvinn)
ringEl.className = "ring"
prikkEl.className = "prikk"

forsvinn();

function forsvinn() {
    ringEl.style.marginLeft = Math.random() * (bredde - 250) + "px"
    ringEl.style.marginTop = Math.random() * (hoyde - 250) + "px"
}

ringEl.appendChild(prikkEl);
bodyEl.appendChild(ringEl);
    </script>
</body>

</html>
