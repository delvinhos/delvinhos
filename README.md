<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        function calcDesconto(){
            let total=quantidade.value*15
            if(quantidade.value >= 1 && quantidade.value <= 5){
                let desconto=total*(2/100)
                let valorFinal=total-desconto
                document.getElementById('apresentaResultado').innerHTML=(valorFinal)
            }else if(quantidade.value > 5 && quantidade.value<=10){
                let desconto=total*(3/100)
                let valorFinal=total-desconto
                document.getElementById('apresentaResultado').innerHTML=(valorFinal)
            }else if(quantidade.value > 10){
                let desconto=total*(5/100)
                let valorFinal=total-desconto
                document.getElementById('apresentaResultado').innerHTML=(valorFinal)
            }else{
                document.getElementById('apresentaResultado').innerHTML=("Quantidade incorreta")
            }
        }
        function converter(){
            document.getElementById('texto').innerHTML=(texto.innerHTML).toUpperCase()
        }
    </script>
</head>
<body>
    <form id="desconto" name="desconto">
        <p id="texto">Calcule o valor das suas compras</p>
        <br>
        <label for="quantidade">Digite a quantidade adquirida</label>
        <br>
        <input type="number" id="quantidade" name="quantidade">
        <span id="apresentaResultado"></span>
        <br>
        <input type="button" id="calcular" name="calcular" value="Valor compra" onclick="calcDesconto()">
        <br>
        <input type="button" id="converte" name="converte" value="Converter" onclick="converter()">
    </form>
</body>
</html>
