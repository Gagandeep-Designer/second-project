# Animated-project

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lunair Eclipse</title>
</head>
<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body{
    height: 100vh;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: #000000;
  }
  h1{
    font-size: 80px;
    font-family: "Roboto", sans-serif;
    font-weight: 900;
    word-spacing: 6px;
    letter-spacing: 9px;
    text-transform: uppercase;
    text-align: center;
    background-image: url(images/sun_image.jpg);
    background-position: center;
   background-size: cover;
   -webkit-background-clip: text;
   color: transparent;
   gap: 50px;
   animation: name  3s ease-in-out infinite;
  }
  @keyframes name{
    0%{
     transform: skewX(60deg);
    }
    100%{
      transform: skew(0deg);
    }
  }
  .container{
    width: 600px;
    height: 600px;
    background: #FDBF60;
    border-radius: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    animation: skychange 10s ease infinite;
  }
  @keyframes skychange{
    0%{
      background-color: #FDBF60;
    }
    25%{
      background-color: #4e3818;
    }
    50%{
      background-color:#000000;
    }
    75%{
      background-color: #4a310b;
    }
    100%{
      background-color: #FDBF60;
    }
  }
  .sun{
    width: 300px;
    height: 300px;
    border-radius: 50%;
    background-color: chocolate;
    position: relative;
    overflow: hidden;

    &::after{
      content: " ";
      width: inherit;
      aspect-ratio: 1;
      background-color: #000000;
      position: absolute;
      top: 0;
      left: 0;
      border-radius: inherit;
      animation: moonwalk 10s ease-in-out infinite;
    }

  }
  @keyframes moonwalk{
    0%{
     translate: 100%;
     scale: 1;
    }  
    50%{
     translate: 0%;
     scale: 0.95;
     box-shadow: rgba(194, 189, 219, 0.5) 0px 48px 100px 0px;
    }
    100%{
     translate: -100%;
     scale: 0.9;
    }
  }
</style>
<body>
  <h1>lunar eclipse</h1>
  <div class="container">
   <div class="sun"></div>
  </div>
</body>
</html>

