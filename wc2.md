---
layout: page
title: WC2
permalink: /web-comp2/
---

### Web Component Test 1

#### With Berlin letter:

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, minimum-scale=1, initial-scale=1, user-scalable=yes" />

    <title>pb-view test2</title>

    <!-- This imports necessary pb-components libraries from unpkg.com -->
    <script src="https://unpkg.com/@webcomponents/webcomponentsjs@2.4.3/webcomponents-loader.js"></script>
    
    <!-- Imports all the components provided by TEI Publisher. -->
    <script type="module" src="https://unpkg.com/@teipublisher/pb-components@latest/dist/pb-components-bundle.js"></script> 
</head>

<body>
    <pb-page endpoint="https://teipublisher.com/exist/apps/tei-publisher">
        <pb-document id="document1" path="test1.xml" odd="dta"></pb-document>
        <!-- Navigate to previous page -->
        <pb-navigation direction="backward" unit="page" keyboard="left">
            <paper-button>
                <iron-icon icon="icons:chevron-left"></iron-icon>
            </paper-button>
        </pb-navigation>
        <pb-view id="view1" src="document1" view="page" column-separator=".tei-cb"></pb-view>
        <!-- Navigate to next page -->
        <pb-navigation direction="forward" unit="page" keyboard="right">
            <paper-button>
                <iron-icon icon="icons:chevron-right"></iron-icon>
            </paper-button>
        </pb-navigation>
    </pb-page>
</body>