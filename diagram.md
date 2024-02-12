```mermaid
erDiagram
    CURSO ||--o{ ALUNO : "inscrito em"
    CURSO ||--o{ UNIDADE_CURRICULAR : "possui"
    PROFESSOR ||--o{ UNIDADE_CURRICULAR : "leciona"
    ALUNO ||--o{ MENSALIDADE : "possui"
