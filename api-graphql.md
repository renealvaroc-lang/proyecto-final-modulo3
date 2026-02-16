# Definición de Esquema GraphQL - Pokémon API

## Tipos Principales

```graphql
type Pokemon {
  id: String!
  name: String!
  weight: Int
  height: Int
  evolutions: [Pokemon]
}