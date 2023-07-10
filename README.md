<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
     <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <title>new slanted navbar</title>
    <style>
        body{
            background-image: url(images/joanna-kosinska-1_CMoFsPfso-unsplash.jpg);
            background-size: cover;
            height: 100vh;
        }
        .container-fluid{
            width: 80%;
            height: 40px;
            position: relative;
            top: 40px;
            margin: 0 auto;
        }
        #logo{
            position: absolute;
            top: 0;     
            left: 0;
            color: white;
            margin-top: -290px;
            font-size: 27px;
            font-family: arial;
        }
        .navigation-wrapper{
            position: relative;

        }
        .navigation-button{
            will-change: transform;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            position: fixed;
            z-index: 1;
            top: 40px;
            right: 100px;
            background: transparent;
            cursor: pointer;

        }
        .navigation-button .fa{
            border: 2px solid white;
            border-radius: 3px;
            padding: 10px;
            color: white;
        }
        .navigation-menu ul li{
            list-style: none;
            font-family: impact;
            font-weight: 300;
            color: hsl(0,0,70%);
        }



        .navigation-menu{
            content: '';
            position: fixed;
            top: 0;
            right: 0;
            width: 50%;
            background: white;
            transform: skew(0deg) translate(100%,0);
            transform-origin: top right;
            transition: all .2s ease-in;
            z-index: -1;
        }



        .navigation-menu ul{
            transform: skewX(-8deg);
            transform-origin: top left;
            position: fixed;
            right: 120px;
            top: 120px;
            width: 400px;
            text-align: right;

        }



        .navigation-menu ul li{
            position: relative;
            z-index: 999;
            font-size: 32px;
            color: hsl(0,0%,10%);
            line-height: 64px;
        }

        .navigation-menu ul li a{
            border: none;
            color: rgb(58, 36, 78);
            text-decoration: none;
        }


        .navigation-menu.active{
            transform: skew(8deg) translate(0,0);
        }


        .navigation-menu li{
            opacity: 0;
            transform: translate(0,10px);
            transition: all .0s ease-in .3s;


        }


        .navigation-menu.active li{
            opacity: 1;
            transform: translate(0,0);
            transition: all 0.2s ease-in 0s;

        } 

        .navigation-menu.active li:nth-child(1){
            transition-delay: .3s;
        } 
        .navigation-menu.active li:nth-child(2){
            transition-delay: .4s;
        } 
        .navigation-menu.active li:nth-child(3){
            transition-delay: .5s;
        } 
        .navigation-menu.active li:nth-child(4){
            transition-delay: .6s;
        } 
        .navigation-menu.active li:nth-child(5){
            transition-delay: .7s;
        } 
        .navigation-menu.active li:nth-child(6){
            transition-delay: .8s;
        } 
        .navigation-menu.active li:nth-child(7){
            transition-delay: .8s;
        } 
        .hero h1{
            margin-top: 270px;
            text-transform: uppercase;
            font-family: impact;
            font-size: 26px;
            letter-spacing: 4px;
            color: white;

        }
        span{
            font-size: 65px;
            letter-spacing: 2px;
            font-family: impact;

        }

        .button{
            font-family: 'Roboto Condensed', sans-serif;
            font-weight: normal;
            font-size: 15px;
            margin-top: 40px;
        }

        .btn1{
            padding: 12px 25px;
            background: #f20c4a;
            text-decoration: none;
            color: white;
            border-top-left-radius: 20px;
            border-bottom-left-radius: 20px;
        }
        .btn2{
            padding: 12px 25px;
            background: #f20c4a;
            text-decoration: none;
            color: white;
            border-top-right-radius: 20px;
            border-bottom-right-radius: 20px;
        }


















    </style>
  </head>
  <body>
    <div class="container-fluid">
        <div id="logo">SRINATH</div>
        <div class="navigation-warpper">
            <div class="navigation-button">
                <i class="fa fa-bars"></i>
            </div>
            <div class="navigation-menu">
                <ul>
                    <li><a href="">HOME</a></li>
                    <li><a href="">GALLERY</a></li>
                    <li><a href="">CONTACT</a></li>
                    <li><a href="">LOCATION</a></li>
                    <li><a href="">TESTIMONIALS</a></li>
                    <li><a href="">PRICING</a></li>
                    <li><a href="">ABOUT US</a></li>
                </ul>

            </div>
        </div>
        <section class="hero">
            <h1>CREATIVE DESIGN <br><span>INTRODUCING</span></h1>
            <div class="button">
                <a href="" class="btn1">GET STARTED</a>
                <a href="" class="btn2">GET FEATURED</a>
            </div>
        </section>
    </div>
    <script>
        var navButton = document.querySelector('.navigation-button');
    var navMenu = document.querySelector('.navigation-menu');
    var win = window;
    
    function openMenu(event) {
      
      navButton.classList.toggle('active');
      navMenu.classList.toggle('active');
    
      event.preventDefault();
      event.stopImmediatePropagation();
    }
      
    function closeMenu(event) {
      if (navButton.classList.contains('active')) {
        navButton.classList.remove('active');
        navMenu.classList.remove('active');
      }
    }
      navButton.addEventListener('click', openMenu, false);
    
    win.addEventListener('click',closeMenu, false);
        
    </script>

    <!-- Optional JavaScript -->
    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
    <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>
  </body>
</html>
