# BlockBattles API Documentation
## Base URL
api.blockbattles.org

## API Endpoints

### Get Stats by Username
- **Endpoint:** `/:apikey/blockbattles/stats/:username`
- **Method:** `GET`
- **Description:** Retrieves player statistics based on the provided username.
- **Parameters:**
  - `apikey`: API key for authentication.
  - `username`: Player's username.

### Get Matches by Username
- **Endpoint:** `/:apikey/blockbattles/matches/:username`
- **Method:** `GET`
- **Description:** Fetches match details for a specified player.
- **Parameters:**
  - `apikey`: API key for authentication.
  - `username`: Player's username.

### Get Leaderboard
- **Endpoint:** `/:apikey/blockbattles/leaderboard`
- **Method:** `GET`
- **Description:** Provides the leaderboard sorted by player ELO.
- **Parameter:**
  - `apikey`: API key for authentication.

### Get All Player Statistics
- **Endpoint:** `/:apikey/blockbattles/allstats`
- **Method:** `GET`
- **Description:** Retrieves statistics for all players.
- **Parameter:**
  - `apikey`: API key for authentication.

### Get Clans
- **Endpoint:** `/:apikey/blockbattles/clans`
- **Method:** `GET`
- **Description:** Fetches information on all clans.
- **Parameter:**
  - `apikey`: API key for authentication.

### Get Clan Details
- **Endpoint:** `/:apikey/blockbattles/clan/:clanName`
- **Method:** `GET`
- **Description:** Provides detailed information about a specific clan.
- **Parameters:**
  - `apikey`: API key for authentication.
  - `clanName`: Name of the clan.

## Rate Limiting
- **Limit:** 100 requests per 15 minutes for each API key.
- **Over Limit Message:** "Too many requests, please try again later."

## Examples

Below are examples of requests and responses to the BlockBattles API:

### Example: Get Clan Details

- **Request:**
GET /{apikey}/blockbattles/clan/BlockBattles

- **Response:**
```json
{
  "clan_id": 3,
  "clan_name": "BlockBattles",
  "leader_uuid": "6ceb560a-5ff4-4e8d-9dcc-527625241245",
  "clan_elo": 0,
  "clan_description": "Person98 is the best dev",
  "is_open": 1,
  "creation_date": "2023-11-25T00:00:00.000Z",
  "members": [
    {
      "member_uuid": "6ceb560a-5ff4-4e8d-9dcc-527625241245",
      "role": "Leader"
    },
    {
      "member_uuid": "525bb7fa-3f98-430f-93ba-112771f285e6",
      "role": "Member"
    }
  ]
}
```
(Note: Replace {apikey} with the actual API key for making requests.)


This section provides a clear example of how to make a request to a specific endpoint of your API and shows the format of the expected response. Remember to replace `{apikey}` with an actual or obfuscated API key when presenting real examples.

