```mermaid

sequenceDiagram
participant browser
participant server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
server-->>browser: HTML document

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->>browser: the css file

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
server-->>browser: the javascript file

Note right of browser: Browser executes the javascript code to render the page dynamically

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->>browser: JSON data of notes

Note right of browser: javascript renders the notes on the page