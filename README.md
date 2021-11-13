
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">


    <title>Hamburger</title>
   
</head>
     <style>
      
  * { 
     margin: 0;
     padding: 0;
     box-sizing:border-box;

  }
  body {
    
     background:#0D067C;
     display:flex;
     justify-content:center;
     align-items:center;
     min-height:100vh;
  }



   .menu-btn {
       position:relative;
       display:flex;
       justify-content:center;
       align-items:center;
       width:80px;
       height:80px;
       cursor:pointer;
       transition: all .5s ease-in-out;
       border: 10px ;
       background-color:#0D067C;
       border-radius:40px;
       box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.363);
       
   } 
   .menu-btn_burguer {
       width:50px;
       height:6px;
       background:linear-gradient(to right, #04FFFF , #FF2CE2);
       border-radius:5px;
       box-shadow: 0 2px 5px rgba(255, 101, 47, .2);
       transition: all .5s ease-in-out;
     
   }
   .menu-btn_burguer::before,
   .menu-btn_burguer::after {
     content: '';
     position:absolute;
     width:50px;
     height:6px;
     background:linear-gradient(to right, #04FFFF , #FF2CE2);;
     border-radius:5px;
     box-shadow: 0 2px 5px rgba(255, 101, 47, .2);
     transition: all .5s ease-in-out;
   }
   .menu-btn_burguer::before {
     transform: translateY(-16px);
   }
   .menu-btn_burguer::after {
     transform: translateY(16px);
   }
   /*Animação*/
   .menu-btn.open .menu-btn_burguer {
      transform: translateX(-50px);
      background: transparent;
      box-shadow: none;
   }
   .menu-btn.open .menu-btn_burguer::before{
      transform: rotate(45deg) translate(35px, -35px);
   }
   .menu-btn.open .menu-btn_burguer::after{
       transform:rotate(-45deg) translate(35px, 35px);
   }
     
     
     </style>
<body>
     
     <div class="menu-btn">
       <div class="menu-btn_burguer"></div>
     </div>
     <script>
       const menuBtn = document.querySelector('.menu-btn');
      
       let menuOpen = false;
       menuBtn.addEventListener('click', () => { 
        if (!menuOpen) {
           menuBtn.classList.add('open');
           menuOpen = true;
        } else {
           menuBtn.classList.remove('open');
           menuOpen = false;
        }
       });
       
     
     </script>
</body>
</html>
