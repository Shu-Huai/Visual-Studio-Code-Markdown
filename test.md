# FM

## [player api](http://s3.s100.vip:35881/docs#/player%20api)

### **GET**[/api/v1/player/](http://s3.s100.vip:35881/docs#/player%20api/get_player_api_v1_player__get) Get Player

获取指定存档的全部球员 :param save_id: 存档id :param skip: 偏移量 :param limit: 一次性返回的数量 :return: list of schemas.player

#### Parameters

| Name                   | Description                |
| ---------------------- | -------------------------- |
| save_id*integer(query) | [ ]                        |
| skipinteger(query)     | *Default value* : 0[ ]   |
| limitinteger(query)    | *Default value* : 100[ ] |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "id": 0,
    "club_id": 0,
    "name": "string",
    "translated_name": "string",
    "translated_nationality": "string",
    "age": 0,
    "height": 0,
    "weight": 0,
    "birth_date": "string",
    "wages": 0,
    "real_stamina": 100,
    "ST_num": 0,
    "CM_num": 0,
    "LW_num": 0,
    "RW_num": 0,
    "CB_num": 0,
    "LB_num": 0,
    "RB_num": 0,
    "GK_num": 0,
    "CAM_num": 0,
    "LM_num": 0,
    "RM_num": 0,
    "CDM_num": 0,
    "shooting": 0,
    "passing": 0,
    "dribbling": 0,
    "interception": 0,
    "pace": 0,
    "strength": 0,
    "aggression": 0,
    "anticipation": 0,
    "free_kick": 0,
    "stamina": 0,
    "goalkeeping": 0,
    "top_capa": 0,
    "top_location": "string",
    "location_capa": {
      "additionalProp1": 0,
      "additionalProp2": 0,
      "additionalProp3": 0
    }
  }
]
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | *No links* |
```

### **GET**[/api/v1/player/{player_id}](http://s3.s100.vip:35881/docs#/player%20api/get_player_by_id_api_v1_player__player_id__get)Get Player By Id

获取指定id的球员 :param player_id: 球员id :return: schemas.playerShow

#### Parameters

Try it out

| Name                    | Description |
| ----------------------- | ----------- |
| player_id*integer(path) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
{
  "id": 0,
  "club_id": 0,
  "name": "string",
  "translated_name": "string",
  "translated_nationality": "string",
  "age": 0,
  "height": 0,
  "weight": 0,
  "birth_date": "string",
  "wages": 0,
  "real_stamina": 100,
  "ST_num": 0,
  "CM_num": 0,
  "LW_num": 0,
  "RW_num": 0,
  "CB_num": 0,
  "LB_num": 0,
  "RB_num": 0,
  "GK_num": 0,
  "CAM_num": 0,
  "LM_num": 0,
  "RM_num": 0,
  "CDM_num": 0,
  "shooting": 0,
  "passing": 0,
  "dribbling": 0,
  "interception": 0,
  "pace": 0,
  "strength": 0,
  "aggression": 0,
  "anticipation": 0,
  "free_kick": 0,
  "stamina": 0,
  "goalkeeping": 0,
  "top_capa": 0,
  "top_location": "string",
  "location_capa": {
    "additionalProp1": 0,
    "additionalProp2": 0,
    "additionalProp3": 0
  }
}
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | *No links* |
```

### **GET**[/api/v1/player/{player_id}/game-data](http://s3.s100.vip:35881/docs#/player%20api/get_game_player_data_api_v1_player__player_id__game_data_get)Get Game Player Data

获取指定球员某赛季的比赛信息 :param player_id: 球员id :param start_season: 开始赛季，若为空，默认1开始 :param end_season: 结束赛季，若为空，默认当前赛季

#### Parameters

Try it out

| Name                       | Description |
| -------------------------- | ----------- |
| player_id*integer(path)    | [ ]         |
| start_seasoninteger(query) | [ ]         |
| end_seasoninteger(query)   | [ ]         |
| save_id*integer(query)     | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "location": "ST",
    "final_rating": 0,
    "actions": 0,
    "shots": 0,
    "goals": 0,
    "assists": 0,
    "passes": 0,
    "pass_success": 0,
    "dribbles": 0,
    "dribble_success": 0,
    "tackles": 0,
    "tackle_success": 0,
    "aerials": 0,
    "aerial_success": 0,
    "saves": 0,
    "save_success": 0
  }
]
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                                                  | *No links* |
```

### **GET**[/api/v1/player/{player_id}/total-game-data](http://s3.s100.vip:35881/docs#/player%20api/get_total_game_player_data_api_v1_player__player_id__total_game_data_get)Get Total Game Player Data

获取指定球员某赛季的统计比赛信息 :param player_id: 球员id :param start_season: 开始赛季，若为空，默认1开始 :param end_season: 结束赛季，若为空，默认当前赛季

#### Parameters

Try it out

| Name                       | Description |
| -------------------------- | ----------- |
| player_id*integer(path)    | [ ]         |
| start_seasoninteger(query) | [ ]         |
| end_seasoninteger(query)   | [ ]         |
| save_id*integer(query)     | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
{
  "location": "ST",
  "final_rating": 0,
  "actions": 0,
  "shots": 0,
  "goals": 0,
  "assists": 0,
  "passes": 0,
  "pass_success": 0,
  "dribbles": 0,
  "dribble_success": 0,
  "tackles": 0,
  "tackle_success": 0,
  "aerials": 0,
  "aerial_success": 0,
  "saves": 0,
  "save_success": 0
}
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                          | *No links* |
```

### **GET**[/api/v1/club/{club_id}/player](http://s3.s100.vip:35881/docs#/player%20api/get_players_by_club_api_v1_club__club_id__player_get)Get Players By Club

获取指定俱乐部的球员信息 :param club_id: 俱乐部 id :param save_model: 存档实例 :return: list of schemas.PlayerShow

#### Parameters

Try it out

| Name                   | Description |
| ---------------------- | ----------- |
| club_id*integer(path)  | [ ]         |
| save_id*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "id": 0,
    "club_id": 0,
    "name": "string",
    "translated_name": "string",
    "translated_nationality": "string",
    "age": 0,
    "height": 0,
    "weight": 0,
    "birth_date": "string",
    "wages": 0,
    "real_stamina": 100,
    "ST_num": 0,
    "CM_num": 0,
    "LW_num": 0,
    "RW_num": 0,
    "CB_num": 0,
    "LB_num": 0,
    "RB_num": 0,
    "GK_num": 0,
    "CAM_num": 0,
    "LM_num": 0,
    "RM_num": 0,
    "CDM_num": 0,
    "shooting": 0,
    "passing": 0,
    "dribbling": 0,
    "interception": 0,
    "pace": 0,
    "strength": 0,
    "aggression": 0,
    "anticipation": 0,
    "free_kick": 0,
    "stamina": 0,
    "goalkeeping": 0,
    "top_capa": 0,
    "top_location": "string",
    "location_capa": {
      "additionalProp1": 0,
      "additionalProp2": 0,
      "additionalProp3": 0
    }
  }
]
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | *No links* |
```

### [club api](http://s3.s100.vip:35881/docs#/club%20api)

### **GET**[/api/v1/club/{club_id}](http://s3.s100.vip:35881/docs#/club%20api/get_club_by_id_api_v1_club__club_id__get)Get Club By Id

获取指定id的俱乐部信息 :param club_id: 俱乐部 id

#### Parameters

Try it out

| Name                  | Description |
| --------------------- | ----------- |
| club_id*integer(path) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
{
  "id": 0,
  "name": "string",
  "finance": 0,
  "reputation": 0,
  "assistant": 0,
  "doctor": 0,
  "scout": 0,
  "negotiator": 0,
  "formation": "string",
  "wing_cross": 0,
  "under_cutting": 0,
  "pull_back": 0,
  "middle_attack": 0,
  "counter_attack": 0
}
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                            | *No links* |
```

### **GET**[/api/v1/club/](http://s3.s100.vip:35881/docs#/club%20api/get_club_api_v1_club__get)Get Club

获取指定存档的所有俱乐部信息 :param save_id: 存档 id

#### Parameters

Try it out

| Name                   | Description |
| ---------------------- | ----------- |
| save_id*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "id": 0,
    "name": "string",
    "finance": 0,
    "reputation": 0,
    "assistant": 0,
    "doctor": 0,
    "scout": 0,
    "negotiator": 0,
    "formation": "string",
    "wing_cross": 0,
    "under_cutting": 0,
    "pull_back": 0,
    "middle_attack": 0,
    "counter_attack": 0
  }
]
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                | *No links* |
```

### **GET**[/api/v1/club/{club_id}/player](http://s3.s100.vip:35881/docs#/club%20api/get_players_by_club_api_v1_club__club_id__player_get)Get Players By Club

获取指定俱乐部的球员信息 :param club_id: 俱乐部 id :param save_model: 存档实例 :return: list of schemas.PlayerShow

#### Parameters

Try it out

| Name                   | Description |
| ---------------------- | ----------- |
| club_id*integer(path)  | [ ]         |
| save_id*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "id": 0,
    "club_id": 0,
    "name": "string",
    "translated_name": "string",
    "translated_nationality": "string",
    "age": 0,
    "height": 0,
    "weight": 0,
    "birth_date": "string",
    "wages": 0,
    "real_stamina": 100,
    "ST_num": 0,
    "CM_num": 0,
    "LW_num": 0,
    "RW_num": 0,
    "CB_num": 0,
    "LB_num": 0,
    "RB_num": 0,
    "GK_num": 0,
    "CAM_num": 0,
    "LM_num": 0,
    "RM_num": 0,
    "CDM_num": 0,
    "shooting": 0,
    "passing": 0,
    "dribbling": 0,
    "interception": 0,
    "pace": 0,
    "strength": 0,
    "aggression": 0,
    "anticipation": 0,
    "free_kick": 0,
    "stamina": 0,
    "goalkeeping": 0,
    "top_capa": 0,
    "top_location": "string",
    "location_capa": {
      "additionalProp1": 0,
      "additionalProp2": 0,
      "additionalProp3": 0
    }
  }
]
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | *No links* |
```

### **GET**[/api/v1/league/{league_id}/club](http://s3.s100.vip:35881/docs#/club%20api/get_clubs_by_league_api_v1_league__league_id__club_get)Get Clubs By League

获取指定联赛的所有俱乐部信息

#### Parameters

Try it out

| Name                    | Description |
| ----------------------- | ----------- |
| league_id*integer(path) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "id": 0,
    "name": "string",
    "finance": 0,
    "reputation": 0,
    "assistant": 0,
    "doctor": 0,
    "scout": 0,
    "negotiator": 0,
    "formation": "string",
    "wing_cross": 0,
    "under_cutting": 0,
    "pull_back": 0,
    "middle_attack": 0,
    "counter_attack": 0
  }
]
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                | *No links* |
```

### [user api](http://s3.s100.vip:35881/docs#/user%20api)

### **POST**[/api/v1/user/](http://s3.s100.vip:35881/docs#/user%20api/create_user_api_v1_user__post)Create User

注册用户

#### Parameters

Try it out

No parameters

#### Request body

application/json

* Example Value
* Schema

```json
{
  "email": "string",
  "is_active": true,
  "password": "string"
}
```

#### Responses

#### Curl

```bash
curl -X 'POST' \
  'http://s3.s100.vip:35881/api/v1/user/' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "email": "1",
  "is_active": true,
  "password": "1"
}'
```

#### Request URL

```
http://s3.s100.vip:35881/api/v1/user/
```

#### Server response

| Code | Details                     |
| ---- | --------------------------- |
| 200  | ##### Response bodyDownload |

```json
{
  "email": "1",
  "is_active": true,
  "id": 2
}
```

##### Response headers

```
 access-control-allow-credentials: true  access-control-allow-origin: *  access-control-expose-headers: *  connection: keep-alive  content-length: 37  content-type: application/json  date: Mon,20 Dec 2021 03:05:02 GMT  keep-alive: timeout=4  proxy-connection: keep-alive  server: uvicorn 
```

|

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
{
  "email": "string",
  "is_active": true,
  "id": 0
}
```

```
                              | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

### **GET**[/api/v1/user/save](http://s3.s100.vip:35881/docs#/user%20api/get_saves_by_user_api_v1_user_save_get)Get Saves By User

获取用户存档

#### Parameters

Try it out

No parameters

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "created_time": "2021-12-20T11:03:05.001874",
    "time": "2020-08-01",
    "season": 1,
    "id": 0,
    "user_id": 0,
    "player_club_id": 0
  }
]
```

| *No links* |

### **POST**[/api/v1/user/save](http://s3.s100.vip:35881/docs#/user%20api/create_save_api_v1_user_save_post)Create Save

生成存档 :param save_data: 存档信息 :param current_user: 用户 :return: 生成的存档信息

#### Parameters

Try it out

No parameters

#### Request body

application/json

* Example Value
* Schema

```json
{
  "type": "five_leagues",
  "player_club_name": "阿森纳"
}
```

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
{
  "created_time": "2021-12-20T11:03:05.001874",
  "time": "2020-08-01",
  "season": 1,
  "id": 0,
  "user_id": 0,
  "player_club_id": 0
}
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                | *No links* |
```

### **GET**[/api/v1/user/save/date](http://s3.s100.vip:35881/docs#/user%20api/get_save_date_api_v1_user_save_date_get)Get Save Date

获取当前存档内的时间

#### Parameters

Try it out

| Name                   | Description |
| ---------------------- | ----------- |
| save_id*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
"string"
```

```
                                                                              | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

### [league api](http://s3.s100.vip:35881/docs#/league%20api)

### **GET**[/api/v1/league/](http://s3.s100.vip:35881/docs#/league%20api/get_leagues_api_v1_league__get)Get Leagues

获取指定存档中的所有俱乐部信息

#### Parameters

Try it out

| Name                   | Description |
| ---------------------- | ----------- |
| save_id*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "id": 0,
    "name": "string",
    "cup": "string",
    "points": 0
  }
]
```

```
  | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

### **GET**[/api/v1/league/{league_id}](http://s3.s100.vip:35881/docs#/league%20api/get_league_by_id_api_v1_league__league_id__get)Get League By Id

获取指定联赛的信息

#### Parameters

Try it out

| Name                    | Description |
| ----------------------- | ----------- |
| league_id*integer(path) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
{
  "id": 0,
  "name": "string",
  "cup": "string",
  "points": 0
}
```

```
                  | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

### **GET**[/api/v1/league/{league_id}/club](http://s3.s100.vip:35881/docs#/league%20api/get_clubs_by_league_api_v1_league__league_id__club_get)Get Clubs By League

获取指定联赛的所有俱乐部信息

#### Parameters

Try it out

| Name                    | Description |
| ----------------------- | ----------- |
| league_id*integer(path) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
[
  {
    "id": 0,
    "name": "string",
    "finance": 0,
    "reputation": 0,
    "assistant": 0,
    "doctor": 0,
    "scout": 0,
    "negotiator": 0,
    "formation": "string",
    "wing_cross": 0,
    "under_cutting": 0,
    "pull_back": 0,
    "middle_attack": 0,
    "counter_attack": 0
  }
]
```

| *No links* |
| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

```
                                                                                                                                                                                                                | *No links* |
```

### **GET**[/api/v1/league/{league_id}/points-table](http://s3.s100.vip:35881/docs#/league%20api/get_points_table_api_v1_league__league_id__points_table_get)Get Points Table

获取指定赛季指定联赛的积分榜 :param save_id: 存档id :param game_season: 赛季 :param league_id: 联赛id :return:

#### Parameters

Try it out

| Name                       | Description |
| -------------------------- | ----------- |
| league_id*(path)           | [ ]         |
| save_id*integer(query)     | [ ]         |
| game_season*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
"string"
```

```
                                                                              | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

### **GET**[/api/v1/league/{league_id}/player-chart](http://s3.s100.vip:35881/docs#/league%20api/get_player_chart_api_v1_league__league_id__player_chart_get)Get Player Chart

获取指定赛季指定联赛的球员数据榜 :param save_id: 存档id :param game_season: 赛季 :param league_id: 联赛id

#### Parameters

Try it out

| Name                       | Description |
| -------------------------- | ----------- |
| league_id*(path)           | [ ]         |
| save_id*integer(query)     | [ ]         |
| game_season*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
"string"
```

```
                                                                              | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

### [test api](http://s3.s100.vip:35881/docs#/test%20api)

### **GET**[/api/v1/test/protocol](http://s3.s100.vip:35881/docs#/test%20api/show_protocol_api_v1_test_protocol_get)Show Protocol

展示协议内容

#### Parameters

Try it out

No parameters

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
"string"
```

| *No links* |

### **GET**[/api/v1/test/clear_db](http://s3.s100.vip:35881/docs#/test%20api/clear_db_api_v1_test_clear_db_get)Clear Db

清空数据库中的所有内容

#### Parameters

Try it out

No parameters

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
"string"
```

| *No links* |

### [login api](http://s3.s100.vip:35881/docs#/login%20api)

### **POST**[/api/v1/login/](http://s3.s100.vip:35881/docs#/login%20api/login_api_v1_login__post)Login

#### Parameters

Try it out

No parameters

#### Request body

application/x-www-form-urlencoded

| grant_typestringpattern: password |   |
| --------------------------------- | - |
| username*string                   |   |
| password*string                   |   |
| scopestring                       |   |
| client_idstring                   |   |
| client_secretstring               |   |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
{
  "access_token": "string",
  "token_type": "string"
}
```

```
                             | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

### [next turn api](http://s3.s100.vip:35881/docs#/next%20turn%20api)

### **GET**[/api/v1/next-turn/](http://s3.s100.vip:35881/docs#/next%20turn%20api/next_turn_api_v1_next_turn__get)Next Turn

#### Parameters

Try it out

| Name                    | Description |
| ----------------------- | ----------- |
| save_id*integer(query)  | [ ]         |
| turn_num*integer(query) | [ ]         |

#### Responses

| Code | Description                                                                                     | Links |
| ---- | ----------------------------------------------------------------------------------------------- | ----- |
| 200  | Successful ResponseMedia typeapplication/jsonControls `Accept` header.*Example Value* Schema |       |

```json
"string"
```

```
                                                                              | *No links* |
```

| 422  | Validation ErrorMedia typeapplication/json*Example Value* Schema

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

| *No links* |

#### Schemas

**Body_login_api_v1_login__post**{| grant_type    | **string**`<br/>`title: **Grant Type**`<br/>`pattern: **password** |
| --------------- | -------------------------------------------------------- |
| username***** | **string**`<br/>`title: **Username**                         |
| password***** | **string**`<br/>`title: **Password**                         |
| scope         | **string**`<br/>`title: **Scope**`<br/>`default:                   |
| client_id     | **string**`<br/>`title: **Client Id**                        |
| client_secret | **string**`<br/>`title: **Client Secret**                    |
|               |

}

**ClubShow**{| id*****             |**integer**`<br/>`title:**Id**|
| --------------------- | -------------------------------------------------- |
| name*****           | **string**`<br/>`title: **Name**                       |
| finance*****|**number**`<br/>`title:**Finance**|
| reputation*****     | **number**`<br/>`title: **Reputation**                 |
| assistant           | **integer**`<br/>`title: **Assistant**`<br/>`default: **0**  |
| doctor              | **integer**`<br/>`title: **Doctor**`<br/>`default: **0**     |
| scout               | **integer**`<br/>`title: **Scout**`<br/>`default: **0**      |
| negotiator          | **integer**`<br/>`title: **Negotiator**`<br/>`default: **0** |
| formation*****|**string**`<br/>`title:**Formation**|
| wing_cross*****     | **integer**`<br/>`title: **Wing Cross**                |
| under_cutting*****|**integer**`<br/>`title:**Under Cutting**|
| pull_back*****      | **integer**`<br/>`title: **Pull Back**                 |
| middle_attack*****|**integer**`<br/>`title:**Middle Attack**             |
| counter_attack***** | **integer**`<br/>`title: **Counter Attack**            |
|                     |

}

**GamePlayerDataShow**{| location*****        |**Location**string`<br/>`title:**Location**An enumeration.**Enum:**`<br/>`Array [ 12 ] |
| ---------------------- | ----------------------------------------------------------------------------- |
| final_rating*****    | **number**`<br/>`title: **Final Rating**                                          |
| actions*****|**integer**`<br/>`title:**Actions**|
| shots*****           | **integer**`<br/>`title: **Shots**                                                |
| goals*****|**integer**`<br/>`title:**Goals**|
| assists*****         | **integer**`<br/>`title: **Assists**                                              |
| passes*****|**integer**`<br/>`title:**Passes**|
| pass_success*****    | **integer**`<br/>`title: **Pass Success**                                         |
| dribbles*****|**integer**`<br/>`title:**Dribbles**|
| dribble_success***** | **integer**`<br/>`title: **Dribble Success**                                      |
| tackles*****|**integer**`<br/>`title:**Tackles**|
| tackle_success*****  | **integer**`<br/>`title: **Tackle Success**                                       |
| aerials*****|**integer**`<br/>`title:**Aerials**|
| aerial_success*****  | **integer**`<br/>`title: **Aerial Success**                                       |
| saves*****|**integer**`<br/>`title:**Saves**                                                |
| save_success*****    | **integer**`<br/>`title: **Save Success**                                         |
|                      |

}

**HTTPValidationError**{| detail | **Detail**[...] |
| -------- | ----------------- |
|        |

}

**LeagueShow**{| id*****     |**integer**`<br/>`title:**Id**|
| ------------- | ------------------------------ |
| name*****   | **string**`<br/>`title: **Name**   |
| cup*****|**string**`<br/>`title:**Cup**    |
| points***** | **number**`<br/>`title: ### **POints** |
|             |

}

**Location**string
title: **Location**An enumeration.

Enum:
Array [ 12 ]

**PlayerShow**{| description:                | 返回给前端的球员数据                                |
| ----------------------------- | ----------------------------------------------------- |
| id*****                     |**integer**`<br/>`title:**Id**|
| club_id*****                | **integer**`<br/>`title: **Club Id**                      |
| name*****|**string**`<br/>`title:**Name**|
| translated_name*****        | **string**`<br/>`title: **Translated Name**               |
| translated_nationality*****|**string**`<br/>`title:**Translated Nationality**|
| age*****                    | **integer**`<br/>`title: **Age**                          |
| height*****|**integer**`<br/>`title:**Height**|
| weight*****                 | **integer**`<br/>`title: **Weight**                       |
| birth_date*****|**string**`<br/>`title:**Birth Date**|
| wages                       |**number**`<br/>`title:**Wages**`<br/>`default:**0**|
| real_stamina                |**number**`<br/>`title:**Real Stamina**`<br/>`default:**100**|
| ST_num                      |**integer**`<br/>`title:**St Num**`<br/>`default:**0**|
| CM_num                      |**integer**`<br/>`title:**Cm Num**`<br/>`default:**0**|
| LW_num                      |**integer**`<br/>`title:**Lw Num**`<br/>`default:**0**|
| RW_num                      |**integer**`<br/>`title:**Rw Num**`<br/>`default:**0**|
| CB_num                      |**integer**`<br/>`title:**Cb Num**`<br/>`default:**0**|
| LB_num                      |**integer**`<br/>`title:**Lb Num**`<br/>`default:**0**|
| RB_num                      |**integer**`<br/>`title:**Rb Num**`<br/>`default:**0**|
| GK_num                      |**integer**`<br/>`title:**Gk Num**`<br/>`default:**0**|
| CAM_num                     |**integer**`<br/>`title:**Cam Num**`<br/>`default:**0**|
| LM_num                      |**integer**`<br/>`title:**Lm Num**`<br/>`default:**0**|
| RM_num                      |**integer**`<br/>`title:**Rm Num**`<br/>`default:**0**|
| CDM_num                     |**integer**`<br/>`title:**Cdm Num**`<br/>`default:**0**|
| shooting*****               | **number**`<br/>`title: **Shooting**                      |
| passing*****|**number**`<br/>`title:**Passing**|
| dribbling*****              | **number**`<br/>`title: **Dribbling**                     |
| interception*****|**number**`<br/>`title:**Interception**|
| pace*****                   | **number**`<br/>`title: **Pace**                          |
| strength*****|**number**`<br/>`title:**Strength**|
| aggression*****             | **number**`<br/>`title: **Aggression**                    |
| anticipation*****|**number**`<br/>`title:**Anticipation**|
| free_kick*****              | **number**`<br/>`title: **Free Kick**                     |
| stamina*****|**number**`<br/>`title:**Stamina**|
| goalkeeping*****            | **number**`<br/>`title: **Goalkeeping**                   |
| top_capa*****|**number**`<br/>`title:**Top Capa**|
| top_location*****           | **string**`<br/>`title: **Top Location**                  |
| location_capa*****|**Location Capa**{...}                              |
|                             |

}

**SaveData**{| type             | **string**`<br/>`title: **Type**`<br/>`default: **five_leagues**       |
| ------------------ | ------------------------------------------------------------ |
| player_club_name | **string**`<br/>`title: **Player Club Name**`<br/>`default: **阿森纳** |
|                  |

}

**SaveShow**{| created_time        | **string**($date-time)`<br/>`title: **Created Time**`<br/>`default: **2021-12-20T11:03:05.001874** |
| --------------------- | ---------------------------------------------------------------------------------------- |
| time                | **string**`<br/>`title: **Time**`<br/>`default: **2020-08-01**                                     |
| season              | **integer**`<br/>`title: **Season**`<br/>`default: **1**                                           |
| id*****             | **integer**`<br/>`title: **Id**                                                              |
| user_id*****        |**integer**`<br/>`title:**User Id**                                                         |
| player_club_id***** | **integer**`<br/>`title: **Player Club Id**                                                  |
|                     |

}

**Token**{| description:      | token的返回格式                    |
| ------------------- | ------------------------------------ |
| access_token***** | **string**`<br/>`title: **Access Token** |
| token_type*****   |**string**`<br/>`title:**Token Type**   |
|                   |

}

**User**{| email*****     |**string**`<br/>`title:**Email**|
| ---------------- | ---------------------------------- |
| is_active***** | **boolean**`<br/>`title: **Is Active** |
| id*****|**integer**`<br/>`title:**Id**        |
|                |

}

**UserCreate**{| email*****     |**string**`<br/>`title:**Email**|
| ---------------- | ---------------------------------- |
| is_active***** | **boolean**`<br/>`title: **Is Active** |
| password*****|**string**`<br/>`title:**Password**   |
|                |

}

**ValidationError**{| loc*****  |**Location**[...]                |
| ----------- | ---------------------------------- |
| msg*****  | **string**`<br/>`title: **Message**    |
| type*****|**string**`<br/>`title:**Error Type** |
|           |

}
