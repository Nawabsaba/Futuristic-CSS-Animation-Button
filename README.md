# Futuristic-CSS-Animation-Button
Learn how to create a Futuristic CSS Animated Button with modern effects and smooth animations! 💻 In this Short, discover how to design a stylish button using HTML and CSS to make your website look more attractive and professional.

![image alt](https://github.com/Nawabsaba/Futuristic-CSS-Animation-Button/blob/7a6e7ce5c9fcf07a52505d17eb427730fdeb32fa/Button_img.png)


# HTML Program :-
     <!DOCTYPE html>
     <html>
     <head>
          <title> Button Effects javascript</title>
          <link rel="stylesheet" type="text/css" href="style.css">
        </head>
        <body>
        <a href="#">
            <i></i><i></i>
            <span>Button</span>
          </a>
          <script>
              let btn = document.querySelector('a');
              btn.addEventListener('mousemove', e => {
                  let rect = e.target.getBoundingClientRect();
                   let x = e.clientX * 3 - rect.left;
                   btn.style.setProperty('--x', x + 'deg');
              })
            </script>
           </body>
         </html>


# CSS Progrma :-
      @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
      
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
     }

    :root {
       --x: 45deg;
    }

    body {
       display: flex;
       justify-content: center;
       align-items: center;
       min-height: 100vh;
       background: #0e1538;
     }

     a {
       position: relative;
       width: 150px;
       height: 55px;
       display: inline-block;
       border-radius: 5px;
      }

     a i {
       position: absolute;
       inset: -2px;
       display: block;
       border-radius: 5px;
    }

      a i,
      a i:nth-child(2) {
       background: linear-gradient(var(--x), #00ccff, #0e1538,
       #0e1538, #d400d4);
     }


    a i:nth-child(2) {
       filter: blur(10px);
    }

    a span {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      text-transform: uppercase;
      color: #fff;
      letter-spacing: 2px;
      border-radius: 3px;
      background: rgba(14, 21, 56, 0.65);
      overflow: hidden;
    }


    a span::before {
      content: '';
      position: absolute;
      top: 0;
      left: -50%;
      width: 100%;
      height: 100%;
      background: rgba(255, 255, 255, 0.075);
     transform: skew(20deg);
    }
