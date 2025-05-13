# O que foi entendido da aula de computação da semana 4:
### Eu entendi que para buscar informacoes dentro de um bacno de dados que esta organizado em tabelas, onde elas se ligam por meio de chaves, devemos usar JOIN.

## Existem 3 principais tipos de JOIN:

- Inner JOIN
- Left JOIN
- Right JOIN

#### Por meio de chaves primárias (em uma tabela inicial) e das chaves estrangeiras (em outra tabela), que fazem relação a aquela chave primária, conseguimos "filtrar" as informações de duas tabelas.


## Um exemplo de JOIN aplicado no projeto:

```sql
SELECT aluno.id, aluno.nome, aluno.email, curso.nome AS curso
    FROM aluno
    LEFT JOIN curso ON aluno.curso_id = curso.id
    ORDER BY aluno.id ASC
```

#### Nesse exemplo queremos compilar as informacoes de duas tabelas independentes, mas que estão relacionadas por uma chave. A tabela "aluno" e a tabela "curso", neste caso, estão ligadas pela coluna ".id". Após do JOIN teremos as informações do aluno, que já estavam na tabela "aluno" junto com seu curso, que estava na tabela "curso"

