---
layout: page
title: //Test// pb-mei
permalink: /web-comp1/
---

# Test with the pb-mei component including demo files and ddd's files

The fist file is from [MEI Sample Encodings repository](https://github.com/music-encoding/sample-encodings) and the others from from the ddd project. Both are uploaded with a raw.github adress but only the MEI Sample works.

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>TEI Publisher Webcomponents Example</title>
    <script src="https://unpkg.com/@webcomponents/webcomponentsjs@2.4.3/webcomponents-loader.js"></script>
    <script type="module" src="https://unpkg.com/@teipublisher/pb-components@latest/dist/pb-components-bundle.js"></script>
    <script type="module" src="https://unpkg.com/@teipublisher/pb-components@latest/dist/pb-leaflet-map.js"></script>
    <style> 
        @import url('https://fonts.googleapis.com/css?family=Oswald|Roboto&display=swap');
        body {
            margin: 10px 20px;
            font-size: 16px;
            font-family: 'Roboto', 'Noto', sans - serif;
            line-height: 1.42857;
            font-weight: 300;
            color: #333333;
            --paper-tooltip-delay-in: 200;
        }
        pb-mei {
            max-width: 1024px;
            width: 100%;
            max-height: 480px;
            margin: 40px 0;
            padding: 20px 0;
            border-bottom: 1px solid #919191;
            border-top: 1px solid #919191;
        }
        pb-mei:first-child {
            margin-top: 0;
        }
    </style>          
</head>
<body>
    	<pb-page endpoint="https://teipublisher.com/exist/apps/tei-publisher">
		<main>
		    <pb-mei player="true" url="https://raw.githubusercontent.com/music-encoding/sample-encodings/master/MEI_4.0/Music/Complete_examples/Joplin_Elite_Syncopations.mei">
		    </pb-mei>
		    <pb-mei player="true" url="https://raw.githubusercontent.com/adnilem/test-site/main/MEI/RIE1880-0017-02.mei">
		    </pb-mei>
		    <pb-mei player="true" url="https://raw.githubusercontent.com/adnilem/test-site/main/MEI/RIE1880-0017-02.mei">
		    </pb-mei>
            <pb-mei player="true" url="https://raw.githubusercontent.com/adnilem/test-site/main/MEI/WEI1860-0072-02.mei">
		    </pb-mei>
		</main>
	</pb-page>
</body>
