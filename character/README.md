# Character Queries – Rick and Morty GraphQL API

This project demonstrates how to query the **Rick and Morty GraphQL API** to fetch character data in a **paginated format**.

## Objective

Learners will create GraphQL queries to retrieve a paginated list of characters.  
Each query fetches **id, name, status, and image** fields for characters on pages **1–4**.

## Project Structure

```
alx-graphql-0x00/
└── character/
    ├── README.md
    ├── characters-page-1.graphql
    ├── characters-page-1-output.json
    ├── characters-page-2.graphql
    ├── characters-page-2-output.json
    ├── characters-page-3.graphql
    ├── characters-page-3-output.json
    ├── characters-page-4.graphql
    └── characters-page-4-output.json
```

## Queries

Each `.graphql` file contains a query like this (example for page 1):

```graphql
query {
  characters(page: 1) {
    results {
      id
      name
      status
      image
    }
  }
}
```

The same structure is repeated for pages 2, 3, and 4 by changing the `page` argument.

---

## Outputs

Each `.json` file contains the expected API response. Example for **page 1**:

```json
{
  "data": {
    "characters": {
      "results": [
        {
          "id": "1",
          "name": "Rick Sanchez",
          "status": "Alive",
          "image": "https://rickandmortyapi.com/api/character/avatar/1.jpeg"
        },
        {
          "id": "2",
          "name": "Morty Smith",
          "status": "Alive",
          "image": "https://rickandmortyapi.com/api/character/avatar/2.jpeg"
        }
        // ... more characters
      ]
    }
  }
}
```

Outputs for pages 2–4 follow the same structure, with different character data.

---

## How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/<your-username>/alx-graphql-0x00.git
   cd alx-graphql-0x00/character
   ```

2. Use a GraphQL client (like [Apollo Studio](https://studio.apollographql.com/), [Insomnia](https://insomnia.rest/), or [GraphiQL](https://github.com/graphql/graphiql)).

3. Run the query:

   - Copy the contents of `characters-page-1.graphql` into your client.
   - Execute against the Rick and Morty GraphQL endpoint:
     ```
     https://rickandmortyapi.com/graphql
     ```

4. Compare the response with the corresponding `characters-page-1-output.json`.

---
