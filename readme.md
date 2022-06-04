
# Telemedicine

-


## API Reference
- Authen
- Get Profile / Project
- Get All Person Info
- Get All Patient
- Patient Detail
- Add Patient
- Measure Patient Health


## Authen

```http
  POST /v2/auth/token
```
#### Request
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `username` | `string` | **Required**.  |
| `password` | `string` | **Required**.  |
| `grant_type` | `string` | **Required**. [password, refresh_token] |

#### Response
```
{
    "code": 1,
    "message": "success",
    "data": {
        "expired_at": 86399,
        "expired_date": "2021-12-07T06:39:37.489896348Z",
        "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdXRob3JpemVkIjp0cnVlLCJleHAiOjE2Mzg4NTkxNzcsInVzZXJfaWQiOiJiOGIxOWQ5Yy1jNWQwLTRhZmYtOTI0ZC04MTYzMDI0YmM4M2MifQ.XBzcnZpsQ8RajKRKkKmPG6EyqjE7_Lt1mnZZbIDTs10",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdXRob3JpemVkIjp0cnVlLCJleHAiOjE2Mzg4NTkxNzcsInVzZXJfaWQiOjE2Mn0.z0CEs50OkaN-KaPrIYZmdn2-lEANnMRziLtYJeigKSw"
    }
}
```

## Get Profile & Project

```http
  GET /v2/me
```

#### Header
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Authorization`      | `string` | **Required**. Bearer  {access_token} |


#### Request Body
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |



#### Response
```
{
    "code": 1,
    "message": "success",
    "data": {
        "avatar": 0,
        "created_at": "2021-12-01T05:15:49.493Z",
        "date_of_birth": "1974-03-08T00:00:00Z",
        "email": "test@email.com",
        "gender": "test",
        "id": "x",
        "name": "TestSI",
        "phone_number": "TestSI",
        "project": [
            {
                "created_at": "2021-12-01T12:00:11Z",
                "id": "x",
                "name_en": "Smart Infirmary",
                "name_th": "Smart Infirmary",
                "project_key": "x",
                "type": "isolation",
                "updated_at": "2021-12-01T12:00:17Z"
            }
        ],
        "surname": "TestSI",
        "title_name_id": 0,
        "updated_at": "2021-12-01T05:15:49.493Z"
    }
}
```
