<!DOCTYPE html>
<html>

<head>
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <title>Calculator </title>
    <link rel="stylesheet" href="style.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
            box-sizing: border-box;
        }

        .container {
            width: 100%;
            height: 100vh;
            background: rgb(227, 249, 255);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .calculator {
            background: #F0FFFF;
            padding: 20px;
            border-radius: 10px;
        }

        .calculator form input {
            border: 0;
            outline: 0;
            width: 60px;
            height: 60px;
            border-radius: 10px;
            box-shadow: -8px -8px 15px rgba(255, 255, 255, 0.1), 5px 5px 15px rgba(0, 0, 0, 0.2);
            background: #000000;
            font-size: 20px;
            color: #5F9EA0;
            cursor: pointer;
            margin: 10px;
        }

        .display {
            display: flex;
            justify-content: flex-end;
            margin: 20px 0;
        }

        .display input {
            text-align: right;
            flex: 1;
            font-size: 45px;
            box-shadow: none;
        }

        .equal {
            width: 145px;
        }

        .operator {
            color: #7FFF00;
        }
    </style>
</head>

<body>

    <div class="container">
        <div class="calculator">
            <form>
                <div class="display">
                    <input type="text" name="display">
                </div>
                <div>
                    <input type="button" value="AC" onclick="display.value+='' " class="operator">
                    <input type="button" value="DE" onclick="display.value = display.value.toString().slice(0,-1)"
                        class="operator">
                    <input type="button" value="." onclick="display.value+='.' " class="operator">
                    <input type="button" value="/" onclick="display.value+='/' " class="operator">
                </div>
                <div>
                    <input type="button" value="7" onclick="display.value+='7' ">
                    <input type="button" value="8" onclick="display.value+='8' ">
                    <input type="button" value="9" onclick="display.value+='9' ">
                    <input type="button" value="*" onclick="display.value+='*' " class="operator">
                </div>
                <div>
                    <input type="button" value="4" onclick="display.value+='4' ">
                    <input type="button" value="5" onclick="display.value+='5' ">
                    <input type="button" value="6" onclick="display.value+='6' ">
                    <input type="button" value="-" onclick="display.value+='-' " class="operator">
                </div>
                <div>
                    <input type="button" value="1" onclick="display.value+='1' ">
                    <input type="button" value="2" onclick="display.value+='2' ">
                    <input type="button" value="3" onclick="display.value+='3' ">
                    <input type="button" value="+" onclick="display.value+='+' " class="operator">
                </div>
                <div>
                    <input type="button" value="00" onclick="display.value+='00' ">
                    <input type="button" value="0" onclick="display.value+='0' ">
                    <input type="button" value="=" class="equal" onclick="display.value =eval(display.value)"
                        class="operator">

                </div>
            </form>
        </div>
    </div>
</body>

</html>

