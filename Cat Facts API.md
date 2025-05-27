# Cat Facts API

Cat Facts API is a simple public API that gives the user random cat-related facts. It is a great tool for educational purposes or demo projects.

## Base URL

`https://catfact.ninja`

## Authentication

No API key or authentication required. Just send a GET request.


## Endpoints

### 1. Get A Random Cat Fact

**Endpoint:**  
`GET /fact`

**Example Request:**  
`GET https://catfact.ninja/fact`

**Example Response:**

```json
{
  "fact": "Cats can rotate their ears 180 degrees.",
  "length": 42
}
```

### 2. Get Multiple Cat Facts

**Endpoint:**  
`GET /facts`

**Query Parameters:**
- `limit`: Number of facts to return (e.g., 3)
- `max_length`: Maximum number of characters per fact (e.g., 100)

**Example Request:**  
`GET https://catfact.ninja/facts?limit=2&max_length=100`

**Example Response:**

```json
{
  "data": [
    { "fact": "Cats sleep 70% of their lives.", "length": 35 },
    { "fact": "A group of cats is called a clowder.", "length": 41 }
  ],
  "current_page": 1,
  "last_page": 34
}
```

### 3. Get Cat Breeds

**Endpoint:**  
`GET /breeds`

**Example Request:**  
`GET https://catfact.ninja/breeds`

**Example Response:**

```json
{
  "data": [
    {
      "breed": "Abyssinian",
      "country": "Ethiopia",
      "origin": "Natural",
      "coat": "Short",
      "pattern": "Ticked"
    },
    {
      "breed": "Bengal",
      "country": "United States",
      "origin": "Hybrid",
      "coat": "Short",
      "pattern": "Spotted"
    }
  ]
}
```

## Request & Response Examples

### 1. Requesting a Single Cat Fact

**Request:**
`GET https://catfact.ninja/fact`

**Response:**

```json
{
  "fact": "Cats have five toes on their front paws, but only four on the back ones.",
  "length": 75
}
```
### 2. Requesting Multiple Cat Facts

**Request:**
`GET https://catfact.ninja/facts?limit=3`

**Response:**

```json
{
  "data": [
    { "fact": "A cat can jump up to six times its length.", "length": 45 },
    { "fact": "Cats have over 20 muscles that control their ears.", "length": 53 },
    { "fact": "Cats purr at a frequency that promotes healing.", "length": 49 }
  ],
  "current_page": 1,
  "last_page": 34
}
```

### 3. Requesting Cat Breeds

**Request:** 
`GET https://catfact.ninja/breeds`

**Response:**

```
{
  "data": [
    {
      "breed": "Siamese",
      "country": "Thailand",
      "origin": "Natural",
      "coat": "Short",
      "pattern": "Colorpoint"
    },
    {
      "breed": "Maine Coon",
      "country": "United States",
      "origin": "Natural",
      "coat": "Long",
      "pattern": "Tabby"
    }
  ]
}
```
## Error Handling

The Cat Facts API returns standard HTTP status codes.

### Common Errors

- **404 Not Found** – The requested endpoint does not exist.  
  _Example:_ A typo in `/factz` instead of `/fact`

- **400 Bad Request** – Invalid query parameters (rare)

- **500 Internal Server Error** – If something goes wrong on the server side (uncommon)

No detailed error messages are returned in the JSON body. Always check your endpoint spelling and query parameters.

## Usage Tips
- ✅ **No authentication required** – Great for beginners as no API key required.
- 🚫 **No rate limits are documented**, however it's good practice not to flood the server with requests.
- 🐾 Perfect for testing API clients, starting beginner projects, or adding some whimsical content to an app.
- 📄 For more information or updates, visit the official site: [https://catfact.ninja](https://catfact.ninja)

## Changelog

### v1.0 – May 2025
- Initial release
- Documented `/fact`, `/facts` and `/breeds` endpoints
- Added overview and usage tips
