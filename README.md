
# TANZANIA MIKOA API

 Welcome to mikoa API documentation, the API is prepared to help make it easy fetch any region,
                districts,wards and streets. 
                We are creating an online portal where users can help fill in missing data and it will be reflected after aproval by the moderation Team.


## Acknowledgements

 - [Zepson Technologies](http://zepson.co.tz/)

 - [Alpha Olomi](https://github.com/alphaolomi)
 - [Jordan Kelebu](https://github.com/Kalebu)

 


## Authors

- [@Zepson Technologies](https://github.com/Zepson-Technologies)
- [@pro-cms](https://github.com/pro-cms)

## API Reference

### BASE URL 

```
BASE URL: http://mikoa.kitivopoint.com

```

#### Get all regions

```http
  GET /api/v1/regions
```
 
 ##### sample response

 ```json
[
    {
        "id": 1,
        "name": "Shinyanga",
        "code": "37",
        "created_at": "2021-11-07T15:18:52.000000Z",
        "updated_at": "2021-11-07T15:18:52.000000Z"
    },
    {
        "id": 2,
        "name": "Mara",
        "code": "31",
        "created_at": "2021-11-07T15:19:00.000000Z",
        "updated_at": "2021-11-07T15:19:00.000000Z"
    },

 ```

#### Get All Districts

```http
  GET /api/v1/districts
```
#### sample response 

```json
[
     {
        "name": "Butiama",
        "code": "312"
    },
    {
        "name": "Rorya",
        "code": "313"
    },: "372"
    },
```

#### Get all Wards

```http
  GET /api/v1/wards
```
 #### sample response

 ```json
[
    {
        "name": "Mjini",
        "code": null
    },
    {
        "name": "Kambarage",
        "code": null
    },
]
 ```

#### Get All Streets

```http
  GET /api/v1/Streets
```
#### sample response

```json

{ 
    "name":"Bugayambelele magharibi",
    "code":"NULL"
    }

```
#### filter district by regions

```http
  GET /api/v1/filter_districts_by_region
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `region`      | `string` | **Required**. Region ID or name |

#### Sample response
```json
 {
        "id": 151,
        "name": "Dodoma\ncbd",
        "code": "411",
        "region_id": 26,
        "created_at": "2021-11-07T15:21:33.000000Z",
        "updated_at": "2021-11-07T15:21:33.000000Z"
    },
    {
        "id": 152,
        "name": "Dodoma",
        "code": "412",
        "region_id": 26,
        "created_at": "2021-11-07T15:21:33.000000Z",
        "updated_at": "2021-11-07T15:21:33.000000Z"
    },
```


 
#### filter ward by district

```http
  GET /api/v1/filter_wards_by_district
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `district`      | `string` | **Required**. District ID or name |

#### Sample response
```json
 {
        "id": 479,
        "name": "Machame mashariki",
        "code": null,
        "district_id": 19,
        "created_at": "2021-11-07T15:19:11.000000Z",
        "updated_at": "2021-11-07T15:19:11.000000Z"
    },
    {
        "id": 480,
        "name": "Machame narumu",
        "code": null,
        "district_id": 19,
        "created_at": "2021-11-07T15:19:11.000000Z",
        "updated_at": "2021-11-07T15:19:11.000000Z"
    },
```

#### filter Street by ward

```http
  GET /api/v1/filter_streets_by_ward
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `ward`      | `string` | **Required**. ward ID or name |

#### Sample response
```json
   {
        "id": 7221,
        "name": "Kibaoni",
        "code": "NULL",
        "ward_id": 490,
        "created_at": "2021-11-07T15:19:11.000000Z",
        "updated_at": "2021-11-07T15:19:11.000000Z"
    },
    {
        "id": 7222,
        "name": "Bomani",
        "code": "NULL",
        "ward_id": 490,
        "created_at": "2021-11-07T15:19:11.000000Z",
        "updated_at": "2021-11-07T15:19:11.000000Z"
    },
```

#### Get All regions with district

```http
  GET /api/v1/regions_with_districts
```
 
#### Sample response
```[
    {
        "id": 1,
        "name": "Shinyanga",
        "code": "37",
        "created_at": "2021-11-07T15:18:52.000000Z",
        "updated_at": "2021-11-07T15:18:52.000000Z",
        "districts": [
            {
                "id": 1,
                "name": "Shinyanga\ncbd",
                "code": "371",
                "region_id": 1,
                "created_at": "2021-11-07T15:18:52.000000Z",
                "updated_at": "2021-11-07T15:18:52.000000Z"
            },
            {
                "id": 2,
                "name": "Shinyanga",
                "code": "372",
                "region_id": 1,
                "created_at": "2021-11-07T15:18:53.000000Z",
                "updated_at": "2021-11-07T15:18:53.000000Z"
            },

```

#### Get All district with ward

```http
  GET /api/v1/districts_with_wards
```

 
#### Sample response
```[
    {
        "id": 1,
        "name": "Shinyanga\ncbd",
        "code": "371",
        "region_id": 1,
        "created_at": "2021-11-07T15:18:52.000000Z",
        "updated_at": "2021-11-07T15:18:52.000000Z",
        "wards": [
            {
                "id": 1,
                "name": "Mjini",
                "code": null,
                "district_id": 1,
                "created_at": "2021-11-07T15:18:52.000000Z",
                "updated_at": "2021-11-07T15:18:52.000000Z"
            },
            {
                "id": 2,
                "name": "Kambarage",
                "code": null,
                "district_id": 1,
                "created_at": "2021-11-07T15:18:52.000000Z",
                "updated_at": "2021-11-07T15:18:52.000000Z"
            },
            
```



#### Get All ward with Street

```http
  GET /api/v1/wards_with_streets
```


#### Get total Regions

```http
  GET /api/v1/total_regions
```
 #### sample response

 ```json
{
    "total": 158
}
 ```

 #### Get total Districts

```http
  GET /api/v1/total_districts
```
 #### sample response

 ```json
{
    "total": 3321
}
 ```


 #### Get total Wards

```http
  GET /api/v1/total_wards
```
 

 
 #### Get total Street

```http
  GET /api/v1/total_streets
```
 
 
#### total district by region

```http
  GET /api/v1/total_districts_by_region
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `region`      | `string` | **Required**. region ID or name |


 
 
#### total ward by district

```http
  GET /api/v1/total_wards_by_district
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `district`      | `string` | **Required**. ID or name |



#### total street by ward

```http
  GET /api/v1/total_streets_by_ward
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `ward`      | `string` | **Required**. ID or name |

