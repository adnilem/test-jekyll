---
layout: page
title: WC2
permalink: /web-comp2/
---
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, minimum-scale=1, initial-scale=1, user-scalable=yes" />
    <title>pb-view Demo</title>
    <script src="https://unpkg.com/@webcomponents/webcomponentsjs@2.4.3/webcomponents-loader.js"></script>
    <script type="module" src="https://unpkg.com/@teipublisher/pb-components@latest/dist/pb-components-bundle.js">
    </script>
    <style>pb-page {
        position: relative;
        }
        pb-view {
            margin-left: auto;
            margin-right: auto;
        }
        #view1 {
            overflow: auto;
            display: flex;
            justify-content: center;
            max-height: calc(100vh - 80px);
        }
        @media (min-width: 769px) {
            pb-view {
                max-width: 60vw;
            }
        }
        footer {
            margin-top: 10px;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: #f2f2f2;
            margin-left: auto;
            margin-right: auto;
        }
        pb-navigation[disabled] {
            display: block;
            visibility: hidden;
        }
        pb-navigation[direction="forward"] {
            float: right;
        }</style>
</head>

<body>
    <pb-page endpoint="https://teipublisher.com/exist/apps/tei-publisher">
        <pb-document id="document1" path="playground/Die_Natur_der_Harmonik_und_der_Metrik_tei.xml" odd="dta"></pb-document>
        <pb-progress></pb-progress>
        <!-- Output the document title -->
        <pb-view src="document1" xpath="//teiHeader/fileDesc/titleStmt/title">
            <pb-param name="header" value="short" />
        </pb-view>
        <pb-view id="view1" src="document1" view="page" append-footnotes animation></pb-view>
        <footer>
            <!-- Navigate to next page -->
            <pb-navigation direction="forward" keyboard="right">
                <paper-button>
                    <iron-icon icon="icons:chevron-right"></iron-icon>
                </paper-button>
            </pb-navigation>
            <!-- Navigate to previous page -->
            <pb-navigation direction="backward" keyboard="left">
                <paper-button>
                    <iron-icon icon="icons:chevron-left"></iron-icon>
                </paper-button>
            </pb-navigation>
        </footer>
    </pb-page>
</body>


This is a direct example taken from TEI-Publisher documentation.
- there must be no empty line within the HTML or it creates problems
- conflict between the web component footer and the jekyll footer
- the whole page reloads when navigating through the document pages
- js and css and in the <head>, sould be moved to separate file

