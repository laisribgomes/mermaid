```mermaid
  erDiagram
      CURSO {
          varchar nome_curso
          int id_curso PK
          int carga_horaria
      }
      ALUNO {
          int registro_academico PK
          varchar nome_aluno
          varchar endereco 
          varchar telefone
          date data_nascimento 
      }
      PROFESSOR {
          int id_professor PK
          varchar nome_professor
      }
  
      UNIDADE_CURRICULAR {
          varchar sigla PK
          varchar nome_unidade_curricular
          char carga_horaria
      }
  
      MENSALIDADE {
          date data_emissao PK
          date data_vencimento
          date data_pagamento
          int valor_mensalidade
      }
    
    CURSO ||--o{ ALUNO : "possui"
    CURSO ||--|{ UNIDADE_CURRICULAR : "possui"
    PROFESSOR ||--|{ UNIDADE_CURRICULAR : "leciona"
    ALUNO ||--|{ MENSALIDADE : "recebe"
