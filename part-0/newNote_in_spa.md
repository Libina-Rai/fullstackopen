```mermaid

sequenceDiagram
participant browser
participant server

note right of browser: user writes a new note and clicks the "save" button. Javascript reads the input and sends it to the server in the background.
browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
server-->>browser: Response with status and confirmation

note right of browser: javascript saves the new node in memory and updates the page to show it without reloading.