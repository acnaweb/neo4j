# Neo4j Graph Database

Neo4j Graph

## Use Cases

- Redes Sociais
- Sistemas de Recomendações
- Sistema de Logística
- Detecção de Fraude
- Controle de Acesso

## Install

Download and Install [Neo4J Desktop](https://neo4j.com/download/neo4j-desktop/)

## Usage

### Run

```sh
docker run \
-p 7474:7474 \
-p 7687:7687 \
-v ./data:/neo4j/data \
-v ./conf:/conf \
-v ./plugins:/plugins \
-v ./backup:/backup \
-e NEO4J_AUTH=neo4j/mypassword \
neo4j:5
```
### Web UI

> * http://localhost:7474/
> * user: neo4j pwd: mypassword

### API

> Neo4j Bolt
> - bolt://localhost:7687/ 
> - user: neo4j 
> - pwd: mypassword

### Cypher Query Language

```sql
CREATE (: Pessoa{nome: "João", idade: 20})
CREATE (: Pessoa{nome: "Maria", idade: 30})
```

```sql
MATCH (p1: Pessoa{nome: "João"}), (p2: Pessoa{nome: "Maria"})
CREATE (p1)-[:SEQUE]->(P2)
```

```sql
MATCH (p: Pessoa{nome: "Maria"}) RETURN p
```

```sql
MATCH (p: Pessoa{nome: "Maria"}) SET p.estadoCivil = "casada"
```

```sql
MATCH (p: Pessoa{nome: "João"}) 
DELETE p
```

```sql
MATCH (p: Pessoa{nome: "João"}) 
DETACH DELETE p
```

### Info

#### RDBMS Vs Graph Database

| RDBMS            | Graph Database            |
|------------------|---------------------------|
| Tables           | Label                    |
| Rows             | Nodes                     |
| Columns and Data | Properties and its values |
| Constraints      | Relationships             |
| Joins            | Transversal               |

## References

- https://neo4j.com/
- https://www.tutorialspoint.com/neo4j/index.htm
- [Introdução ao Neo4j, Grafos, Nós, Rótulos](https://www.youtube.com/watch?v=5jlPSMPLHQ4)
