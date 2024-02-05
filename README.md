# trabalhodastack



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>a.css</title>
    <link rel="stylesheet" href="a.css" type="text/css"/>

    <title>Consulta de CEP</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        form {
            margin-bottom: 20px;
        }
        input[type="text"] {
            padding: 5px;
            width: 200px;
        }
        button {
            padding: 5px 10px;
        }
        #result {
            margin-top: 20px;
        }
    </style>

</head>
<body>



<div class ="container">

    <div class="Menu">
        <img src ="https://img.freepik.com/vetores-premium/conceito-de-palavra-no-blog-de-formas-geometricas-de-cores_205544-12899.jpg"
        width="50px"
        height="50px">

        <hr>
        
       <h1>BLOG HcG</h1>

       <hr>

       <img src ="https://cdn-icons-png.flaticon.com/512/74/74472.png"
       width="40px"
       height="40px">usuario
    
    <hr>


    <img src ="https://cdn-icons-png.flaticon.com/512/1500/1500455.png"
    width="30px"
    height="30px"
    >  <font size="4"> friends </font>
<br>
<br>

<hr>

<img src ="https://cdn-icons-png.flaticon.com/512/149/149852.png"
width="30px"
height="30px"
> <font size="4"> Search </font>
<br>
<br>

<hr>



    
    </div>



    <div class="Dashboard">  <font size="7"> Dashboard </font>
        






    </div>


    <div class="div3">
        <img src="https://i.pinimg.com/originals/e2/9f/9a/e29f9af1680d9c079c05b4e09ce59d8f.jpg"
        width="40px"
        heigth="40px">VIEW SHOP


    </div>

    <div class="div4">

        <h1>Consulta de CEP para calcular o frete</h1>
    <form>
        <label for="cep">CEP:</label>
        <input type="text" id="cep" maxlength="8" placeholder="Digite o CEP" required>
        <button type="submit">Consultar</button>
    </form>
    <div id="result"></div>

    <script>
        const form = document.querySelector('form');
        const inputCep = document.querySelector('#cep');
        const resultDiv = document.querySelector('#result');

        form.addEventListener('submit', function (e) {
            e.preventDefault();
            const cep = inputCep.value;
            consultarCEP(cep);
        });

        function consultarCEP(cep) {
            const url = `https://viacep.com.br/ws/${cep}/json/`;

            fetch(url)
                .then(response => response.json())
                .then(data => {
                    if (data.erro) {
                        mostrarErro('CEP não encontrado');
                    } else {
                        mostrarResultado(data);
                    }
                })
                .catch(error => {
                    mostrarErro('Erro na consulta');
                });
        }

        function mostrarResultado(data) {
            const resultHTML = `
                <p><strong>CEP:</strong> ${data.cep}</p>
                <p><strong>Logradouro:</strong> ${data.logradouro}</p>
                <p><strong>Bairro:</strong> ${data.bairro}</p>
                <p><strong>Cidade:</strong> ${data.localidade}</p>
                <p><strong>Estado:</strong> ${data.uf}</p>
            `;
            resultDiv.innerHTML = resultHTML;
        }

        function mostrarErro(message) {
            resultDiv.innerHTML = `<p class="error">${message}</p>`;
        }
    </script>

    </div>
    
    


    </div>
    

</div>
    
<div class="div7"><h1>PC GAMER</h1>

<img src="https://m.media-amazon.com/images/I/71YA4qtn2JL._AC_UF894,1000_QL80_.jpg"
width="400px"
height="360px"
>


</div>

<div class="div8"><h1>PREÇO</h1>
    <br>
<p><b>400 rS</b></p>
<br>




</div>

<div class="div9">
<h1>CONFIG</h1>
<br>
<p><b>GABINETE GAMER DT3 HYPER VIEW, LATERAL E FRONTAL DE VIDRO</b></p>
<br>



</div>


<div class="div10">
<h1>ENTREGAS</h1>
<br>
<p><b>brasil inteiro</b></p>
<br>
<p>1 dia util para entrega</p>








</div>


</div>

</div>



</div>
</body>
</html>



.container{
    border: x solid white;
    width:1500px;
    background:white;
    height: 250px;

    
    }
    *{
        margin:0;
        padding:0;
    }

    body{
        width: 100%;
        height:100%;
    }
        
    div{
    background: gray;
    
    }
    
    .container > div:nth-child(2n){;}
    
    .Menu {width:200px; height:250px;background-color:white;}
    .Dashboard {width:1100px; height:70px;background-color:white;}
    .div3 {width:200px; height:70px;background-color:white;}
    .div4 {width:1300px; height:70px;background-color: rgb(157, 255, 0);}
  


    .div7 {width:1300px; height:420px;background-color:rgb(225, 225, 225);}    

    .div8 {width:400px;height:125px;background-color:gray;margin-left:440px;margin-top:-190px ;}

    .div9 {width:400px;height:125px;background-color:gray;margin-left:900px;margin-top:-290px ;}

    .div10 {width:400px;height:125px;background-color:gray;margin-left:440px;margin-top:-140px ;}

    

   
   











    
    .container > div {float:left;}





