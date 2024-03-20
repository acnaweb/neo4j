# Neo4j Graph Database

Amundsen Data Catalog

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

> * [Neo4J](http://localhost:7474/) 
> * user: neo4j pwd: mypassword

### API

> Neo4j Bolt
> - bolt://localhost:7687/ 
> - user: neo4j 
> - pwd: mypassword


### Info

#### RDBMS Vs Graph Database

| RDBMS            | Graph Database            |
|------------------|---------------------------|
| Tables           | Graphs                    |
| Rows             | Nodes                     |
| Columns and Data | Properties and its values |
| Constraints      | Relationships             |
| Joins            | Traversal                 |

## References

- https://neo4j.com/
- https://www.tutorialspoint.com/neo4j/index.htm

