# roteadorDB
Roteador para banco de dados Oracle, PgSQL, MySql, etc.


mermaid.sequenceConfig = {
  diagramMarginX: 50,
  diagramMarginY: 10,
  boxTextMargin: 5,
  noteMargin: 10,
  messageMargin: 35,
  mirrorActors: true,
};
<img align="center" alt="Material de Apoio" src="https://img.shields.io/badge/Ver%20Material-E94D5F?style=for-the-badge">

```mermaid
%%{
  init: {
    'theme': 'forest',
    'themeVariables': {
      'lineColor': '#F8B229',
      'secondaryColor': '#006100',
      'tertiaryColor': '#fff',
    }
  
}%%
sequenceDiagram
    
    participant Java_Swing_App as Java Swing App 
    participant roteadorDB
    participant DBMS as Database (DBMS)

    rect rgb(191, 223, 255)
    Java_Swing_App->>roteadorDB: HTTP POST {query, db_type}
    end
    roteadorDB->>DBMS: Connect DB {db_type}
    Note right of roteadorDB: Rational thoughts!
    DBMS-->>roteadorDB: Fetch Data
    roteadorDB-->>Java_Swing_App: JSON {result}
```
