# roteadorDB
Roteador para banco de dados Oracle, PgSQL, MySql, etc.

sequenceDiagram
    participant Java_Swing_App as Java Swing App
    participant roteadorDB
    participant DBMS as Database (DBMS)

    Java_Swing_App->>roteadorDB: HTTP POST {query, db_type}
    roteadorDB->>DBMS: Connect DB {db_type}
    DBMS-->>roteadorDB: Fetch Data
    roteadorDB-->>Java_Swing_App: JSON {result}
