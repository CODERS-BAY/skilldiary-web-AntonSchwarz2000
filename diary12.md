# web day 6

## I started creating the game "Schere-Stein-Papier". 
### It nearly works without any errors or bugs, but up to now the game is only running with alerts. 


    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Schere, Stein, Papier</title>
    <link rel="stylesheet" href="spielStyle.css">
    </head>
    <body>
    <h1>Schere, Stein, Papier</h1>
    <h2>Wähle!</h2>
    <h2>Bei einer Eingabe eines ungültigen Wertes ist das Spiel sofort verloren!

    </h2>
    <script>
        //Variable festlegen
        var symbolComputer;
        var symbolSpieler;
        var anzahlRunden = 0;
        var gewinneComputer = 0;
        var gewinneSpieler = 0;
        var gewinnBedingung = 3;
        
        do {
            //Rundenzähler
            anzahlRunden++;
            alert("Runde" + anzahlRunden)
            
            //Der Computer denkt sich zu Beginn jeder Runde eine Zahl aus
            ausgedacht = Math.random() * 3
            ausgedacht = Math.round(ausgedacht + 0.5)
            
            //Zuordnung für den Computer
            if(ausgedacht == 1) {
                ausgedacht = "Schere"
            };
            
            if(ausgedacht == 2) {
                symbolComputer = "Stein"
            };

            if(ausgedacht == 3) {
                symbolComputer = "Papier"
            };
            
            //Der Spieler muss nun eingeben, was er wählt
            wahlSpieler = prompt("Gib deine Wahl ein", "Schere ist 1, Stein ist 2, Papier ist 3")
            
            //Zuordnung für Spieler
            if(wahlSpieler == 1) {
                symbolSpieler = "Schere"
            };
            if (wahlSpieler == 2) {
                symbolSpieler = "Stein"
            };
            if (wahlSpieler == 3) {
                symbolSpieler = "Papier"
            };
            //Zuordnung, falls ein ungültiger Wert eingegeben wurde
            if (wahlSpieler != 1 && wahlSpieler != 2 && wahlSpieler != 3) {
                alert("Das war ein ungültiger Wert!")
                break
            }
           
            //Vergleich, wer gewonnen hat
            //Hier zuerst, ob ein Unentschieden vorliegt
            if (symbolSpieler == symbolComputer) {
                alert ("Unentschieden");
            }
            
            //Schere gewinnt gegen Papier
            if (symbolComputer == "Schere" && symbolSpieler == "Papier") {
                gewinneComputer++;
                alert("Computer gewinnt mit Schere");
            }
            if (symbolSpieler == "Schere" && symbolComputer == "Papier") {
                gewinneSpieler++;
                alert("Du gewinnst gegen Papier");
            }
            
            //Papier gewinnt gegen Stein
            if (symbolComputer == "Papier" && symbolSpieler == "Stein") {
                gewinneComputer++;
                alert("Computer gewinnt mit Papier");
            }
            if (symbolSpieler == "Papier" && symbolComputer == "Stein") {
                gewinneSpieler++;
                alert("Du gewinnst gegen Stein");
            }
            
            //Stein gewinnt gegen Schere
            if (symbolComputer == "Stein" && symbolSpieler == "Schere") {
                gewinneComputer++;
                alert("Computer gewinnt mit Stein");
            }
            if (symbolSpieler == "Stein" && symbolComputer == "Schere") {
                gewinneSpieler++;
                alert("Du gewinnst gegen Schere");
            }
            
            //Spielstand
            alert(gewinneSpieler + " zu " + gewinneComputer);


        } while (gewinneSpieler < 3 && gewinneComputer < 3) {
         //Ausgabe wer wie oft gewonnen hat
        if (gewinneSpieler>= 3) {
            alert("Du hast das Spiel gewonnen. Gratuliere!")
        }
        else {
            alert("Der Computer war besser und du hast das Spiel leider verloren!")
        }
       
        }
    </script>
    </body>
    </html