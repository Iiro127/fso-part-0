```mermaid
sequenceDiagram
    participant browser
    participant server 

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Note right of browser: Browser sends note data to the server
    activate server
    Note left of server: Server processes this data and saves it to update the notes
    server-->>browser: HTTP 201: {"message":"note created"}
    deactivate server

    Note right of browser: The browser updates the notes on the page without reloading the page
