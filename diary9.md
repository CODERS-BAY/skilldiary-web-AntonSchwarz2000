## web day 4

We joined a presentation about bbw. (bahnbau wels)

I continued working with unit 5.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div id="container">
    <p>
        <dl>
            <dt><dfn>Beatles, The</dfn></dt>
            <dd>Die Beatles waren eine britische Band...</dd>
            <dt>Rolling Stones, The</dt>
            <dd>Die Rolling Stones waren........</dd>
        </dl>
    <p>------------------------------------------------------</p>
    </p>
    <p>Bandmitglieder
        <dl>
            <dt>The Beatles</dt>
            <dd>John</dd>
            <dd>Paul</dd>
            <dd>George</dd>
            <dd>Ringo</dd>
            <dd class="unbekannt">Stuart</dd>
            <dd class="unbekannt">Pete</dd>
        </dl>
    <p>------------------------------------------------------</p>
        <ol>
            <li>Item 1
                <ol>
                    <li>Item 1.1</li>
                    <li>Item 1.2
                        <ul>
                            <li>Item 1.2.1</li>
                            <li>Item 1.2.2
                                <ul>
                                    <li>Item 1.2.2.1</li>
                                    <li>Item 1.2.2.2</li>
                                </ul>
                            </li>
                        </ul>
                    </li>
                </ol>
            </li>
            <li>Item 2
                <ol>
                    <li>Item 2.1</li>
                    <li>Item 2.2</li>
                </ol>
            </li>
            <li>Item 3
                <ol>
                    <li>Item 3.1</li>
                    <li>Item 3.2</li>
                    <li>Item 3.3</li>
                </ol>
            </li>
        </ol>
    </p>
    <p>------------------------------------------------------</p>
    <ol>
        <li>Item 1</li>
            <li><ol>
                <li>Item 1.1</li>
                <li>Item 1.2</li>
                    <li><ul>
                        <li>Item 1.2.1</li>
                    </ul>
                </li>
            </ol>
        </li>
        <li>Item 2</li>
    </ol>
    <p>------------------------------------------------------</p>
    <ol id="zahlen">
        <li>eins</li>
        <li>zwei</li>
        <li>drei</li>
        <li>vier</li>
        <li>fünf</li>
        <li>sechs</li>
    </ol>
    <p>------------------------------------------------------</p>
    <p>
        <ul id="smile">
            <li>prim</li>
            <li>sekund</li>
            <li>terz</li>
            <li>quart</li>
            <li>quint</li>
            <li>sext</li>
            <li>septime</li>
            <li>oktave</li>
        </ul>
</div>
</body>
</html>

<style>
#container {
    margin-inline-start: auto;
    width: 960px;
    }
#zahlen {
    list-style-type: upper-alpha;
}
#smile { 
    list-style-image: url(../src/smile.png);
    image-si: ;
    font-style: oblique;
}
.unbekannt {
    color: lightgray;
}
ol ol>li {
    list-style-type: lower-alpha;
}
ul > li {
    list-style-type: disc;
}
ul > li > ul > li {
    list-style-type: circle;
}
</style>