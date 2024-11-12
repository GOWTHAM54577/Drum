# Drum

### Site URL

https://gowtham54577.github.io/Drum/

### index.html

~~~

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Doto:wght@100..900&family=Montserrat:ital,wght@0,100..900;1,100..900&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Playpen+Sans:wght@100..800&family=Playwrite+CU:wght@100..400&family=Roboto+Slab:wght@100..900&display=swap" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Doto:wght@100..900&family=Merriweather:ital,wght@0,300;0,400;0,700;0,900;1,300;1,400;1,700;1,900&family=Montserrat:ital,wght@0,100..900;1,100..900&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Playpen+Sans:wght@100..800&family=Playwrite+CU:wght@100..400&family=Roboto+Slab:wght@100..900&display=swap" rel="stylesheet">
    <title>Drum</title>
    <style>
        h1{
            text-align: center;
            font-family: "Roboto Slab", serif;
            font-optical-sizing: auto;
            font-weight: 1000 ;
            font-style: normal;
            font-size: 5rem;
            text-shadow:
                    -1px -1px 0 #DE7C7D,  /* Top left */
                    1px -1px 0 #DE7C7D,  /* Top right */
                    -1px  1px 0 #DE7C7D,  /* Bottom left */
                    1px  1px 0 #DE7C7D;  /* Bottom right */
                         
        }
        
        body{
            text-align: center;
            background-color: #AF1740;
        }
        footer{
            margin: 10%;
        }
        
        .w{
            background-image: url('./images/tom1.png');
        }
        .a{
            background-image: url('./images/tom2.png');
        }
        .s{
            background-image: url('./images/tom3.png');
        }
        .d{
            background-image: url('./images/tom4.png');
        }
        .j{
            background-image: url('./images/crash.png');
        }
        .k{
            background-image: url('./images/kick.png');
        }
        .l{
            background-image: url('./images/snare.png');
        }
        .set{
            margin: 10% auto;
        }
        .Drum {
            color: #490000;
            outline: none;
            font-size: 5rem;
            border: 10px solid #DE7C7D;
            border-radius: 15px;
            margin: 20px;
            font-family: "Roboto Slab", serif;
            font-optical-sizing: auto;
            font-weight: 1000 ;
            font-style: normal;
            text-shadow: 
                -1px -1px 0 #DE7C7D,  /* Top left */
                1px -1px 0 #DE7C7D,  /* Top right */
                -1px  1px 0 #DE7C7D,  /* Bottom left */
                1px  1px 0 #DE7C7D;  /* Bottom right */
        }
        button
        {
            width: 200px;
            height : 150px;
        }
        footer{
            font-family: "Merriweather", serif;
            font-weight: 700;
            font-style: normal;
            font-size: 1rem;
            text-shadow:
                    -1px -1px 0 #DE7C7D,  /* Top left */
                    1px -1px 0 #DE7C7D,  /* Top right */
                    -1px  1px 0 #DE7C7D,  /* Bottom left */
                    1px  1px 0 #DE7C7D;  /* Bottom right */
        }
        .pressed{
            box-shadow: 0 3px 4px 0 #dbedf3;
            opacity : 0.5;
        }

        @media(max-width: 480px){
            h1{
                font-size: 3rem;
            }
            button{
                width: 100px;
                height: 75px;
            }
            .Drum{
                font-size: 2rem;
                margin: 12px;
            }
            footer{
                margin-top: 10px;
                font-size: 0.8rem;
            }

        }

        
    </style>
</head>
<body>
    <h1 id="title">Drum 🥁 Kit</h1>
    <div class="set">
        <button class="w W Drum">W</button>
        <button class="a A Drum">A</button>
        <button class="s S Drum">S</button>
        <button class="d D Drum">D</button>
        <button class="j J Drum">J</button>
        <button class="k K Drum">K</button>
        <button class="l L Drum">L</button>
    </div>

    <footer>
        🥁Created  By  GOWTHAM N 🥁
    </footer>
    <script type="text/javascript">
        var numOfButton = document.querySelectorAll(".Drum").length;
        for(let i=0;i<numOfButton;i++)
        {
            document.querySelectorAll(".Drum")[i].addEventListener("click",function (){
                var buttonClicked = this.innerHTML;
                
                soundButton(buttonClicked);
                animationButton(buttonClicked);
            });
        }

        document.addEventListener("keypress",function (events){
            soundButton(events.key);
            animationButton(events.key);
        });

        function soundButton(key){
            var a = key;
            var new_key = a.toLowerCase()
            switch(new_key){
                case 'w':
                    var tom_1 = new Audio("sounds/tom-1.mp3");
                    tom_1.play();
                    break;
                case 'a':
                    var tom_2 = new Audio("sounds/tom-2.mp3");
                    tom_2.play();
                    break;
                case 's':
                    var tom_3 = new Audio("sounds/tom-3.mp3");
                    tom_3.play();
                    break;
                case 'd':
                    var tom_4 = new Audio("sounds/tom-4.mp3");
                    tom_4.play();
                    break;
                case 'j':
                    var crash = new Audio("sounds/crash.mp3");
                    crash.play();
                    break;
                case 'k':
                    var kick = new Audio("sounds/kick-bass.mp3");
                    kick.play();
                    break;
                case 'l':
                    var snare = new Audio("sounds/snare.mp3");
                    snare.play();
                    break;
                default:
                    console.log(buttonClicked);
            }
        }

    

        function animationButton(currentkey){
            var activeButton = document.querySelector("." + currentkey); // Use querySelector for a single element
            activeButton.classList.add("pressed");
            setTimeout(function (){
                activeButton.classList.remove("pressed");
            }, 80);
        }
        
    </script>
</body>
</html>

~~~

### Output:

![image](https://github.com/user-attachments/assets/25a4c750-9366-490d-9431-6f72dd2d39f4)


