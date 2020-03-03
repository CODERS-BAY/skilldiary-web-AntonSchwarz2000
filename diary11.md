## web day 5
We discussed Java Script.

    Things we talked about:
        alert
        var
        let
        document.write
        function
        const
        document.getElementById
        ===
        !==
        parseInt
We discussed Java Script games.

    Games we talked about:
        Handyweitwurf
        Schere Stein Papier
        Zahlen raten
        Code breaker

I worked on the shoes example:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="src/schuhe.js"></script>
</head>
<body>
    <script>
        alert("Deine Schuhe");
    </script>
    <noscript>
        JavaScript ist nicht aktiv
    </noscript>

    <p>
    Regalböden: <input type="text" id="boeden" value="8"/><br/>
    Paare je Boden: <input type="text" id="paare-je-boden" value="5"/><br/>
    Neben dem Regal: <input type="text" id="neben-dem-regal" value="7"/><br/>
    Schrödingers Freundin hat <span id="ausgabe"></span> Schuhe. <br/>
    <button type="button" onclick="zaehleSchuhe();">Klick mich!</button>
    </p>

    
</body>
</html>

<script>
function zaehleSchuhe() {
    var regalboeden = document.getElementById("boeden").value;
    var paareJeBoden = document.getElementById("paare-je-boden").value;
    var paareNebenDemRegal = document.getElementById("neben-dem-regal").value;
    var paare = parseInt(paareNebenDemRegal) + (parseInt(paareJeBoden) * regalboeden);
    var schuhe = paare * 2;
    document.getElementById("ausgabe").innerHTML=schuhe;
}
</script>


I started working on a Java Script game.