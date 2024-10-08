sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: [{"message":"note created"}]
    deactivate server

    Note right of browser: Request Payload: [{ "content": "tio", "date": "2024-10-08T20:52:01.140Z" }]
    Note right of browser: The browser executes the onload function that rerenders the note list on the page and sends the new note to the server            