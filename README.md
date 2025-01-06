<!DOCTYPE html>
<html>
<head>
  <title>FCAFE Server</title>
  <meta name="viewport" content=
  "width=device-width, initial-scale=1">
  <style>
    body {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
        font-family: Tahoma, Verdana, Arial, sans-serif;
        margin: 0;
        background-color: #2c3e50;
        color: #fff;
    }
    form {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 20px;
        background-color: #34495e;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
        border-radius: 10px;
        width: 90%;
        max-width: 300px;
        margin-top: 20px;
    }
    label, input {
        width: 100%;
        margin-top: 10px;
        color: #fff;
    }
    input[type="text"], input[type="password"] {
        padding: 10px;
        background: none;
        border: none;
        border-bottom: 1px solid #bdc3c7;
        color: #ecf0f1;
    }
    input[type="submit"] {
        margin-top: 20px;
        padding: 10px;
        border: none;
        background-color: #e74c3c;
        color: white;
        text-transform: uppercase;
        cursor: pointer;
    }
    input[type="submit"]:hover {
        background-color: #c0392b;
    }
    .output {
        margin: 20px;
        padding: 20px;
        background-color: #34495e;
        border-radius: 10px;
        width: 90%;
        max-width: 300px;
        text-align: justify;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
    }
    .downloads {
        margin-top: 20px;
        padding: 20px;
        background-color: #34495e;
        border-radius: 10px;
        width: 90%;
        max-width: 300px;
        text-align: center;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
    }
    .downloads a {
        display: block;
        color: #1abc9c;
        text-decoration: none;
        margin: 10px 0;
    }
    .downloads a:hover {
        text-decoration: underline;
    }
    @media screen and (max-width: 480px) {
        body {
            font-size: 14px;
        }
    }
  </style>
</head>
<body>
  <audio id="myAudio" autoplay="" muted><source src="moaning.mp3"
  type="audio/mpeg"> Your browser does not support the audio
  element.</audio> 
  <script>

    document.addEventListener('click', function() {
        var x = document.getElementById("myAudio");
        x.muted = false;
        x.play();
        x.volume = 1;
    });
  </script>
  <div class="downloads">
    <h2>Download Config Files</h2><a href=
    "/download.php?file=ec_tcp.ovpn">ec_tcp.ovpn</a> <a href=
    "/download.php?file=ec_udp.ovpn">ec_udp.ovpn</a>
  </div>
  <form id="create-form" action="/create.php" method="post" name=
  "create-form">
    <h2>Create Account</h2><label for="username">Username:</label>
    <input type="text" id="username" name="username" required="">
    <label for="password">Password:</label> <input type="password"
    id="password" name="password" required=""> <input type="submit"
    value="Create">
  </form>
</body>
</html>
