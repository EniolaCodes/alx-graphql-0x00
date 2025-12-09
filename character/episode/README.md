# Episode Query – Rick and Morty GraphQL API

This project demonstrates how to query the **Rick and Morty GraphQL API** to fetch details of a specific episode by ID.

---

## Objective

Learners will write a GraphQL query using the `episode(id: ID!)` field to retrieve details of an episode.  
The query must include the following fields: **id, name, air_date, episode**.

---

## Project Structure

```

alx-graphql-0x00/
└── episode/
├── README.md
├── episode-page-1.graphql
└── episode-page-1-output.json

```

---

## Query Example

```graphql
query {
  episode(id: 1) {
    id
    name
    air_date
    episode
  }
}
```

---

## Output Example

```json
{
  "data": {
    "episode": {
      "id": "1",
      "name": "Pilot",
      "air_date": "December 2, 2013",
      "episode": "S01E01"
    }
  }
}
```

---

## How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/EniolaCodes/alx-graphql-0x00.git
   cd alx-graphql-0x00/episode
   ```

2. Use a GraphQL client (like [Apollo Studio](https://studio.apollographql.com/), [Insomnia](https://insomnia.rest/), or [GraphiQL](https://github.com/graphql/graphiql)).

3. Run the query against the Rick and Morty GraphQL endpoint:

   ```
   https://rickandmortyapi.com/graphql
   ```

4. Compare the response with `episode-page-1-output.json`.

---
