# Decorations
## Get All Decorations
```shell
curl "https://mhw-db.com/decorations"
```

```javascript
fetch('https://mhw-db.com/decorations')
    .then(response => response.json())
    .then(decorations => {
        // your code here
    });
```

> The above command returns an array of [`Decoration`](#decoration-fields) objects.

```json
[
  {
    "id": 1,
    "name": "Antidote Jewel 1",
    "rarity": 5,
    "skills": [
      {
        "id": 1,
        "description": "Reduces the duration of poison by 30%.",
        "level": 1,
        "skill": 1,
        "skillName": "Poison Resistance",
        "modifiers": []
      }
    ],
    "slot": 1
  },
```

This endpoint retrieves all decorations.

### HTTP Request
`GET https://mhw-db.com/decorations`

### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
p | No | See the [Projecting Results](#projecting-results) section
q | No | See the [Searching the API](#searching-the-api) section

### Response
This endpoint returns an array of decorations. For field information, see the [Decoration Fields](#decoration-fields) section.

## Get a Specific Decoration
```shell
curl "https://mhw-db.com/decorations/1"
```

```javascript
fetch('https://mhw-db.com/decorations/1')
    .then(response => response.json())
    .then(decoration => {
        // your code here
    });
```

> The above command returns a single [`Decoration`](#decoration-fields) object.

```json
{
  "id": 1,
  "name": "Antidote Jewel 1",
  "rarity": 5,
  "skills": [
    {
      "id": 1,
      "description": "Reduces the duration of poison by 30%.",
      "level": 1,
      "skill": 1,
      "skillName": "Poison Resistance",
      "modifiers": []
    }
  ],
  "slot": 1
}
```

This endpoint retrieves a specific decoration.


### HTTP Request
`GET https://mhw-db.com/decorations/<id>`

### Path Parameters
Parameter | Type | Description
--------- | ---- | -----------
id | Integer | The ID of the decoration to retrieve

### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
p | No | See the [Projecting Results](#projecting-results) section

### Response
This endpoint returns a single decoration. For field information, see the [Decoration Fields](#decoration-fields) section.

## Decoration Fields
```json
{
  "id": 1,
  "name": "Antidote Jewel 1",
  "rarity": 5,
  "skills": [
    {
      "id": 1,
      "description": "Reduces the duration of poison by 30%.",
      "level": 1,
      "skill": 1,
      "skillName": "Poison Resistance",
      "modifiers": []
    }
  ],
  "slot": 1
}
```

> A sample `Decoration` object.

Field | Type | Description
----- | ---- | -----------
id | Integer | The ID of the decoration
name | String | The name of the decoration
rarity | Integer | The rarity of the decoration
slot | Integer | The slot that the decoration fits into
skills | Array&lt;[SkillRank](#skillrank-fields)&gt; | An array of skill ranks that the decoration provides