## Vehicle Types
> CREATE REQUEST

```json
{
    "name": "Vehicle Type Name",
    "description": "Vehicle Type Description"
}
```

> CREATE RESPONSE

```json
{
    "code": 201,
    "status": "success",
    "message": "Truck vehicle type was added",
    "data": [
        {
            "id": 1,
            "name": "Truck",
            "description": "Vehicle that can transport 5T",
            "created_at": "2022-12-01T08: 12: 22.049585Z",
            "updated_at": "2022-12-01T08: 12: 22.049585Z",
            "deleted_at": null
        }
    ]
}
```
> LIST REQUEST: `https://api.amitruck.co/v2/vehicle-types`

> LIST RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "Vehicle types retrieved successfully",
    "data": [
        {
            "id": 1,
            "name": "Gary Schneider",
            "description": "Represent kitchen I water present",
            "created_at": "2022-12-01T08:24:32.605194Z",
            "updated_at": "2022-12-01T08:24:32.605194Z",
            "deleted_at": null
        },
        {
            "id": 2,
            "name": "Erica Rose",
            "description": "Police number focus foot test.",
            "created_at": "2022-12-01T08:24:32.605194Z",
            "updated_at": "2022-12-01T08:24:32.605194Z",
            "deleted_at": null
        }
    ]
}
```
> RETRIEVE REQUEST  
> GET `https://api.amitruck.co/v2/vehicle-types/1`

> RETRIEVE RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "Truck vehicle type was added",
    "data": [
        {
            "id": 1,
            "name": "Truck",
            "description": "Vehicle that can transport 5T",
            "created_at": "2022-12-01T08: 12: 22.049585Z",
            "updated_at": "2022-12-01T08: 12: 22.049585Z",
            "deleted_at": null
        }
    ]
}
```

> UPDATE REQUEST

```json
{
    "name": "Name Updated",
    "description": "Description Updated"
}
```

>  UPDATE RESPONSE

```json 
{
    "code": 200,
    "status": "success",
    "message": "Vehicle Type successfully updated",
    "data": [
        {
            "id": 42,
            "name": "Name Updated.",
            "description": "Description Updated",
            "created_at": "2022-12-01T08:28:14.683819Z",
            "updated_at": "2022-12-01T08:28:14.687819Z",
            "deleted_at": null
        }
    ]
}
```

> DELETE REQUEST

```json 
{
    "id": 1
}
```

> DELETE RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "Vehicle Type delete successful."
}
```

The vehicle types service allows you to add a new vehicle type in terms of the Trucks, Tuktuk, Bikes, Van or any other vehicle types.
These types are listed on during the vehicle registration page and the vehicle services depend on it. 

This service requires authentication.

#### VEHICLE TYPE PROPERTIES

| Attribute | Type | Description |
| -----------|---------| ----------- |
| id  | Integer | Unique identifier of the resource `readonly` |
| name | string | Vehicle type name |
| description | string | Vehicle type description |
| created_at | date-time | Date time vehicle type was created at `readonly` |
| updated_at | date-time | Date time vehicle type was updated at `readonly` |
| deleted_at | date-time | Date time vehicle type was deleted at |

### CREATE A VEHICLE TYPE

This API is used to add new vehicle types to the Amitruck 2.0 platform. 

* URL: `v2/vehicle-types/create`
* Http Method: `POST`
* Content-Type: `application/json`

### LIST A VEHICLE TYPE

This API returns a collection of all Amitruck 2.0 vehicle types.

* URL: `v2/vehicle-types`
* Http Method: `GET`

### RETRIEVE A VEHICLE TYPE

This endpoint retrieves details of an existing vehicle type. You have to pass the `ID` of the vehicle type. It returns error 404(not found) if the vehicle type to be retrieved does not existing in the Amitruck 2.0 database.

* URL: `v2/vehicle-types/{ID}`
* Http Method: `GET`

### UPDATE A VEHICLE TYPE

This endpoint updates an existing vehicle type. It returns error 404 when the vehicle type to be updated does not exist.

* URL: `v2/vehicle-types/{vehicle-type-ID}/update`
* Http Method: `PUT`
* Content-Type: `application/json`

### DELETE A VEHICLE TYPE

This endpoint DELETES an existing vehicle type in a software way. It does not erase it from the database, instead it updates the `deleted_at` field with the current time stamp so that this field will be considered deleted, but can be restored when needed. 

The API to restore a deleted field will be released in the future version of this API.

* URL: `v2/vehicle-types/{vehicle-type-ID}/delete`
* Http Method: `DELETE`
* Content-Type: `application/json`
