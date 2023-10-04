# Practica-ORM-Avanzada-Avanzada
En esta ocasión explotaremos el potencial de la API GraphQL.

## Sobre la práctica
Se solicita que habiliten un servidor GraphQL en su proyecto de inventario previo y que implementen el siguiente esquema:

type Query {
inventory: [Inventory!]!
inventoryByFlavor(flavor: String!): [Inventory!]!
inventoryByShop(shop: String!): [Inventory!]!
inventoryByDate(date: String!): [Inventory!]!
}

type Mutation {
addInventory(inventory: InventoryInput!): Inventory!
}

input InventoryInput {
shop: ShopInput!
employee: EmployeeInput!
icecream: IcecreamInput!
date: String!
}

input IcecreamInput {
flavor: String!
count: Int!
is_season_flavor: Boolean!
}

input ShopInput {
name: String!
}

input EmployeeInput {
name: String!
}
type Icecream {
flavor: String!
count: Int!
is_season_flavor: Boolean!
}
