# Menu-3D
ejercicio de menú en 3d solo con HTML y CSS por lo que no necesitas instalar dependencias.


**Este es el codigo HTML:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menu 3D</title>
    <link rel ="stylesheet" href="./index.css">
</head>
<body>
    <ul>
        <li style="--i:6;"><a href="#">Home</a></li>
        <li style="--i:5;"><a href="#">About</a></li>
        <li style="--i:4;"><a href="#">Services</a></li>
        <li style="--i:3;"><a href="#">Portafolio</a></li>
        <li style="--i:2;"><a href="#">Our Team</a></li>
        <li style="--i:1;"><a href="#">Contact</a></li>
    </ul>
</body>
</html>
```
**Este es el codigo CSS:**

```CSS
@import url('https://fonts.googleapis.com/css?family=Oswald:400,700');


*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Oswald', sans-serif;
}

body{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

ul{
    position: relative;
    transform: skewY(-15deg)
}

ul li{
    position: relative;
    list-style: none;
    width:200px;
    background: #3e3f46;
    padding:15px;
    z-index: var(--i);
    transition: 0.5s
}

ul li:hover{
    background: #33a3ee;
    transform: translateX(50px);
}

ul li::before{
    content: '';
    position: absolute;
    top:0;
    left: -40px;
    width:40px;
    height: 100%;
    background: #2e3133;
    transform-origin: right;
    transform: skewY(45deg);
    transition: 0.5s
}

ul li:hover::before{
    background: #1f5378
}
ul li:hover::after{
    background: #2982b9

}

ul li::after{
    content: '';
    position: absolute;
    top:-40px;
    left: 0px;
    width:100%;
    height: 40px;
    background: #35383e;
    transform-origin: bottom;
    transform: skewx(45deg);
    transition: 0.5s
}

ul li a{
    text-decoration: none;
    color: #999;
    display: block;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    transition: 05.s
}

ul li a:hover{
    color: #fff
}

ul li:last-child::after{
    box-shadow: -120px 120px 20px rgba(0,0,0,0.35)
}



```
