<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: pink;
            flex-direction: column;
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }
        .yes {
            background-color: red;
            color: white;
        }
        .no {
            background-color: gray;
            color: white;
            position: absolute;
        }
        .gif-container {
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Will you be my Valentine? 💖</h2>
        <button class="yes" onclick="yesClicked()">Yes</button>
        <button class="no" onmouseover="moveButton(this)">No</button>
        <div class="gif-container" id="gifContainer">
            <img id="gif1" src="https://media.giphy.com/media/Z21HJj2kz9uBG/giphy.gif" alt="Valentine Gif 1" style="display: none;">
            <img id="gif2" src="https://media.giphy.com/media/eiRpSPB8OSGVcbkOIJ/giphy.gif" alt="Valentine Gif 2" style="display: none;">
        </div>
    </div>
    
    <script>
        function yesClicked() {
            document.getElementById("gifContainer").style.display = "block";
            document.getElementById("gif1").style.display = "block";
            setTimeout(() => {
                document.getElementById("gif2").style.display = "block";
            }, 2000);
        }
        
        function moveButton(button) {
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
    </script>
</body>
</html>
# index.html
