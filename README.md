<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="Project" href="pro.css">
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animated Login Form</title>
  <style>
    @keyframes fall {
  0% { transform: translateY(-100%); }
  100% { transform: translateY(100%); } 
  0% { top: -100%; }
  100% { top:83%;}
 
}
@keyframes moveLeftToRight {
  0% { transform: translateX(0); }
  100% { transform: translateX(100vw); }
}
@keyframes moveRightToLeft {
  0% { transform: translateX(100vw); }
  100% { transform: translateX(0); }
}
@keyframes animateGirl {
			0% { transform: translateX(100%) rotateY(0); }
			50% { transform: translateX(-100%) rotateY(180deg); }
			100% { transform: translateX(100%) rotateY(360deg); }
		}
		.girl {
			position: absolute;
			bottom: 0;
			left: 0;
			animation: animateGirl 10s linear infinite;
      box-shadow: 10 10px 10px rgba(0, 0, 0, 0);
      

}
		body {
			margin: 0;
			padding: 0;
			overflow-x: hidden;
		}


    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #f0f2f5;
      background-size:100%100% ;
    background-size: auto;
      background: url("trees.png"), url("bg.jpg");
      
    }
 
    .login-container {
      width: 400px;
      padding: 40px;
    background: transparent;
    backdrop-filter: blur(20px);
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
      border-radius: 10px;
   
    }
    .login-container form{
        opacity: 100%;
        justify-content: center;
        align-items: center;
    
    }

    .login-container h2 {
      text-align: center;
      margin-bottom: 30px;
      color: #6d0808;
    }

    .input-container {
      position: relative;
      margin-bottom: 30px;
    }

    .input-container label {
      position: absolute;
      top: 0;
      left: 0;
      color: #6d0808;
      pointer-events: none;
      transition: all 0.3s ease;
    }

    .input-container input {
      width: 100%;
      padding: 10px 10px 10px 0;
      border: none;
      border-bottom: 2px solid #6d0808;
      outline: none;
      font-size: 16px;
      color: #333;
      background: transparent;
    }

    .input-container input:focus ~ label,
    .input-container input:valid ~ label {
      top: -20px;
      left: 0;
      color: #6d0808;
      font-size: 12px;
    }

    .login-container button {
      width: 100%;
      padding: 10px;
      border: none;
      background:#6d0808;
      color: #fff;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px;
      opacity: 100%;
      transition: background 0.3s ease;
      
    }

    .login-container button:hover {
      background: #6d0808;
    }

    .login-container .forgot {
      text-align: center;
      margin-top: 15px;
    }

    .login-container .forgot a {
      color:#6d0808;
      text-decoration: none;
    }

    .login-container .forgot a:hover {
      text-decoration: underline;
    }
    section.girl
{
    position: absolute;
    scale: 0.65;
    animation: animatedGirl 10s linear infinite;
}
@keyframes animateGirl
{
    0%
    {
        transform:translatex(calc(100% + 100vw));
    }  
    50%
    {
        transform:translatex(calc(-100% - 100vw));
    }
    50.01%
    {
        transform:translatex(calc(-100% - 100vw))rotateY(180deg);
    }
    100%
    {
        transform:translatex(calc(100% + 100vw))rotateY(180deg);
    }
}

  </style>
</head>
<body>
  <img src="girl.png" class="girl"style="position: absolute;">

  
  <div style="height: 100vh; ">
<img src="leaf_01.png" style="position: absolute; left: 10%; animation: fall 5s linear infinite; animation-delay: 0s;;">
<img src="leaf_01.png" style="position: absolute; left: 95%; animation: fall 5s linear infinite; animation-delay: 0s;">
<img src="leaf_02.png" style="position: absolute; left: 40%; animation: fall 5s linear infinite; animation-delay: 1s;">
<img src="leaf_02.png" style="position: absolute; left: 80%; animation: fall 5s linear infinite; animation-delay: 1s;">
<img src="leaf_03.png" style="position: absolute; left: 70%; animation: fall 5s linear infinite; animation-delay: 2s;">
<img src="leaf_03.png" style="position: absolute; left: 25%; animation: fall 5s linear infinite; animation-delay: 2s;">
<img src="leaf_04.png" style="position: absolute; left: 90%; animation: fall 5s linear infinite; animation-delay: 3s;">
<img src="leaf_04.png" style="position: absolute; left: 5%; animation: fall 5s linear infinite; animation-delay: 3s;">
  </div>
  <div class="login-container">
    <h2>Login</h2>
    <form>
      <div class="input-container">
        <input type="text" required>
        <label>Username</label>
      </div>
      <div class="input-container">
        <input type="password" required>
        <label>Password</label>
      </div>
      <button type="submit">Login</button>
      <div class="forgot">
        <a href="#">Forgot your password?</a>
      </div>
    </form>
  </div>
</body>
</html>
