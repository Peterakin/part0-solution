```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: Server processes the new note
    server-->>browser: 201 Created (with new note data)
    deactivate server

    Note right of browser: The browser updates the UI to show the new note without reloading the page
```
