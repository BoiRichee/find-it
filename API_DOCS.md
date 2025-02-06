[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=17687847&assignment_repo_type=AssignmentRepo)
# Find-It! (Server Side)

> Tuliskan API Docs kamu di sini

# Products API Documentation

## Endpoints :

List of available endpoints:

- `POST /creategame`
- `POST /joingame`
- `GET /waitplayer`
- `GET /startgame`
- `POST /action`
- `GET /getplayercards`
- `GET /getdeckcards`
- `GET /getscoreboard`
- `GET /getgamestate`

&nbsp;

## 1. POST /creategame

Description:

- Create a new game

Request:

- body:

```json
{
  "username": "string"
}
```

_Response (200 - OK)_

```json
{
  "id": "integer",
  "UserId": "integer",
  "GameId": "integer",
  "playerCards":"array"
}
```

_Response (400 - Bad Request)_

```json
{
  "message": "Username is required"
}
```

&nbsp;

## 2. POST /joingame

Description:

- Join a game

Request:

- body:

```json
{
  "username": "string",
  "GameId": "integer"
}
```

_Response (200 - OK)_

```json
{
  "id": "integer",
  "UserId": "integer",
  "GameId": "integer",
  "playerCards":"array"
}
```

_Response (400 - Bad Request)_

```json
{
  "message": "Game is already in prrogress"
}
OR
{
  "message": "Game has ended"
}
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
```

&nbsp;

## 3. GET /waitPlayer

Description:

- Wait for another player to join the game

_Response (200 - OK)_

```json
{
  "players": "players",
  "message": "string"
}
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
```

&nbsp;

## 4. GET /startgame

Description:

- Start the game

_Response (200 - OK)_

```json
[
  {
    "players": "integer",
    "game": "array"
  },
]
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
```

_Response (400 - Bad Request)_

```json
{
  "message": "Game is already in progress"
}
OR
{
    "message": "Game has ended"
}
OR
{
    "message": "Not enough players to start the game"
}
```

&nbsp;

## 5. POST /action

Request:

- body:

```json
{
  "GameId": "integer",
  "UserId": "integer",
  "ImageId": "integer",
}
```

_Response (200 - OK)_

```json
{
  "players": "integer",
  "game": "array"
}
```

_Response (400 - Bad Request)_

```json
{
  "message": "Game has not started yet"
}
OR
{
  "message": "Game has ended"
}
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
OR
{
    "message": "Player not found"
}
```

&nbsp;

## 6. GET /getplayercards

Description:

- Get player cards

Request:

- body:

```json
{
  "GameId": "integer",
  "UserId": "integer",
}
```

_Response (200 - OK)_

```json
{
  "playerCards": "integer"
}
```

_Response (400 - Bad Request)_

```json
{
  "message": "Game has not started yet"
}
OR
{
  "message": "Game has ended"
}
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
OR
{
    "message": "Player not found"
}
```

&nbsp;

## 7. GET /getdeckcards

Description:

- Get deck cards

Request:

- body:

```json
{
  "GameId": "integer",
}
```

_Response (200 - OK)_

```json
{
  "deckCards": "integer"
}
```

_Response (400 - Bad Request)_

```json
{
  "message": "Game has not started yet"
}
OR
{
  "message": "Game has ended"
}
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
```

&nbsp;

## 8. GET /getscoreboard

Description:

- Get scoreboard

Request:

- body:

```json
{
  "GameId": "integer",
}
```

_Response (200 - OK)_

```json
{
  "playerScores": "integer"
}
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
```

&nbsp;

## 9. GET /getgamestate

Description:

- Get game state

Request:

- body:

```json
{
  "GameId": "integer",
}
```

_Response (404 - Not Found)_

```json
{
  "message": "Game not found"
}
```

&nbsp;