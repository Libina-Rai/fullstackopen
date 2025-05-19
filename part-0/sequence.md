```mermaid

sequenceDiagram
    participant browser
    participant server
    Note right of browser: user writes a new node and clicks the "save" button.
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    server-->>browser: Redirect to /exampleapp/notes

    Note right of browser: Browser makes a new GET request to load the page again
 
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    server-->>browser: browser: HTML document

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->>browser: the css file

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server-->>browser: the JavaScript file

    Note right of browser: Browser executes JavaScript to fetch and render the updated list of notes

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->>browser: Updated JSON with all notes including the new one

     Note right of browser: Browser executes callback to render updated notes
 