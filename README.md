# task_oasis3
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset ="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie-edge">
    <link rel="stylesheet" href="style.css">
    <title>Degree Converter</title>
</head>
<body>

    <h1>Temperature Converter</h1>
    <input type="text" id="fahrenheit" placeholder="Fahrenheit" name="f" value="" />
    <input type="text" id="celsius" placeholder="Celsius" name="c" value="" />
    <button id="convert">Convert!</button>
    <button id="clear">Reset</button>



    <script src="index.js"></script>
</body>
</html>
 28 changes: 28 additions & 0 deletions28  
degree_converter/index.js
@@ -0,0 +1,28 @@
document.getElementById('convert').onclick = tempConvert;
document.getElementById('clear').onclick = clearForm;

function tempConvert() {

    var fahrenheit = document.getElementById("fahrenheit").value;
    var celsius = document.getElementById("celsius").value;

  if (fahrenheit != '') {
        celsius = (parseFloat(fahrenheit) - 32) / 1.8;
    } else {
        fahrenheit = (parseFloat(celsius) * 1.8) + 32;
    }



    document.getElementById('fahrenheit').value = parseFloat(fahrenheit).toFixed(1);
    document.getElementById('celsius').value = parseFloat(celsius).toFixed(1);
}


function clearForm() {
    document.getElementById('fahrenheit').value = '';
    document.getElementById('celsius').value = '';
} 



 51 changes: 51 additions & 0 deletions51  
degree_converter/style.css
@@ -0,0 +1,51 @@
*{
    padding:0;
    margin:0px;
    box-sizing: border-box;
}
body{
    width:100vw;
    height: 100vh;
    display:grid;
    place-items:center;
    background-image: url(https://www.gannett-cdn.com/media/2022/06/09/USATODAY/usatsports/gettyimages-1323823418.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}


#convert {
    background-color: #bba768;
  }
  #convert:hover {
    background-color: #bcc768;
  }
  h1 {
    font-family: sans-serif;
    color: red;
  }
  input {
    display: block;
    padding: 10px;
    margin-top: 10px;
    font-size: 2em;
    color: #f4a55a;
    font-family: cursive, sans-serif;
  }
  ::-webkit-input-placeholder {
     color: #ccc;
  }
  :-moz-placeholder { /* Firefox 18- */
     color: #ccc;  
  }
  ::-moz-placeholder {  /* Firefox 19+ */
     color: #ccc;  
  }
  :-ms-input-placeholder {  
     color: #ccc;  
  }
  button {
    padding: 10px;
    font-size: 1.2em;
    color: #545454;
  }
