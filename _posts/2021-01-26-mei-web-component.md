---
layout: post
title:  "TEI Publisher | Web Component with MEI files"
date:   2021-01-26 15:33 +0100
categories: test web component
---

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
		    <pb-mei player="true" url="https://raw.githubusercontent.com/music-encoding/sample-encodings/master/MEI_4.0/Music/Complete_examples/Liszt_Four_little_pieces.mei">
		    </pb-mei>
		    <pb-mei player="true" url="https://raw.githubusercontent.com/music-encoding/sample-encodings/master/MEI_4.0/Music/Complete_examples/Joplin_Elite_Syncopations.mei">
		    </pb-mei>
		    <pb-mei player="true" url="https://raw.githubusercontent.com/music-encoding/sample-encodings/master/MEI_4.0/Music/Complete_examples/Grieg_op.43_butterfly.mei">
		    </pb-mei>
		</main>
	</pb-page>
</body>