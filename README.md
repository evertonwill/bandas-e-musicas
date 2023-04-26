# bandas-e-musicas
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Test</title>
<style>
    body{text-align: center; background-image: url('Taylor-AD12e-SB-Credit-Adam-Gasson-HERO@2560x1625.jpg') ;font-family: Verdana}
</style>
</head>
<body>
    <h1 id="menu">
    <p>MUSICBOX</p>
        <form  action="" method="get" action="envio de dados">
        <input type="text" id="text" name="nome" placeholder="digite aqui">
        
        <input type="button" type="submit" name="enviar" value="enviar" id="data">
        
        <br><br>

    Banda: <select name=banda id="banda" onchange="jukebox()" >
               <option value=0>Opções</option>
              
                </select>
                <button type="button" id="delete" ;>Remover</button>
                <button type="button">Alterar</button>
                <br>

        Música: <select name=musica id="musica">
               <option value=0></option>
            
            </select>
            <button  type="button" id="delete2">Remover</button>
            <button type="button";>Alterar</button>
        
        </select>
    </form> 
    </h1>
    <script>
    /* Envio de dados Para o Select 1*/

    document.getElementById("data").onclick=function(){
        let pegar=document.getElementById("banda");
        let opcao=document.createElement('Option');
        let entrada=document.getElementById('text');

        opcao.value=entrada.value;
        opcao.text=entrada.value;

        banda.add(opcao);
        entrada.value=""
    }
/*Botão de apagar*/

    document.getElementById("delete").onclick=function(){
    let banda=document.getElementById("banda");

    banda.remove(banda.selectedIndex);
}
document.getElementById("delete2").onclick=function(){
    let musica=document.getElementById("musica");

    musica.remove(musica.selectedIndex);
}
/*Opções de Música*/

function jukebox(){
        var selectBanda=document.getElementById("banda");
        var selectMusica=document.getElementById("musica");
        var filhos = selectMusica.children;
        console.log(filhos);
        selectMusica.innerHTML="";
        var OPC =document.createElement("option");
        OPC.innerHTML="Selecione Uma Música";
        OPC.value ="0";
        selectMusica.appendChild(OPC);

    switch(selectBanda.value){
    case "Paralamas do Sucesso":
        var opc1 = document.createElement("option");
        opc1.innerHTML = "Busca Vida";
        opc1.value = "1";
        selectMusica.appendChild(opc1)

        var opc2 = document.createElement("option");
        opc2.innerHTML="Trac-Trac";
        opc2.value="2";
        selectMusica.appendChild(opc2);
         
        var opc3= document.createElement("option");
        opc3.innerHTML="Lanterna dos Afogados";
        opc3.value="3";
        selectMusica.appendChild(opc3);
        break;
        case "Tears For Fears":
        var opc1 = document.createElement("option");
        opc1.innerHTML = "Shout";
        opc1.value = "1";
        selectMusica.appendChild(opc1)

        var opc2 = document.createElement("option");
        opc2.innerHTML="The Working Hour";
        opc2.value="2";
        selectMusica.appendChild(opc2);
         
        var opc3= document.createElement("option");
        opc3.innerHTML="Head Over Heels";
        opc3.value="3";
        selectMusica.appendChild(opc3);

    }}
   
    
    </script>
</body>
</html>
