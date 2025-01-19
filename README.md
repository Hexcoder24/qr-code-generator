#qr code generator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QR code generator</title>
    <style>
        body, html{
            margin: 0;
            padding: 0;
            height: 100%;

        }
        .container{
            background-color: aqua;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
            flex-direction: column;
        }
            .input{
                background-color: white ;
                padding: 50px 100px;
                border-radius: 20px;
                text-align: center;
                border: 5px solid;


            }
            p{
                font-size: 200%;

            }
            input{
                height: 50px;
                width: 250px;
                border-radius: 20px;
            }
            button{
                background-color:white;
                padding: 10px 80px;
                border-radius: 20px;
                
            }
            button:hover{
                background-color: aqua;
                transform: scale(1.05)

            }

        
    </style>
</head>
<body>
    <div class="container">
        <div class="input">
            <p>QR CODE generator</p>
            <input type="text" id="inputtext" placeholder="Enter QR Code"><br><br>
            <button onclick="generate()"> Generate QR</button><br>

        </div>
        <div class="qr">
            <div class="img">
                <img src="" alt="Image">
            </div>
        </div>
        <div class="qr">
            <div class="img">

            </div>
        </div>
    </div>
    <script>
        let inputtext = document.getElementById("inputtext");
        let imgqr = document.createElement("imgqr");
        function generate() {
            imgqr.src = "https://api.qrserver.com/v1/create-qr-code/?size=150x150&data= "+inputtext;

        }
    </script>
</body>
</html>
