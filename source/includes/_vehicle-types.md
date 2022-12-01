## Vehicle Types


> Create a vehicle type request:

```json
{
    "name": "Vehicle Type Name",
    "description": "Vehicle Type Description"
}
```

> Create a Vehicle Type Response

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
> List Vehicle Type Request: `https://api.amitruck.co/v2/vehicle-types`

> List Vehicle Type Response:

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
> Retrieve A Vehicle Type Request:  GET `https://api.amitruck.co/v2/vehicle-types/1`

> Retrieve A Vehicle Type Response

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

> Update an Existing Vehicle Type Request

```json
{
    "name": "Name Updated",
    "description": "Description Updated"
}
```

>  Update Response

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

> Delete a Vehicle Type Request

```json 
{
    "id": 1
}
```

> Delete a Vehicle Type Response

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

### Vehicle Type Properties

| Attribute | Type | Description |
| -----------|---------| ----------- |
| id  | Integer | Unique identifier of the resource `readonly` |
| name | string | Vehicle type name |
| description | string | Vehicle type description |
| created_at | date-time | Date time vehicle type was created at `readonly` |
| updated_at | date-time | Date time vehicle type was updated at `readonly` |
| deleted_at | date-time | Date time vehicle type was deleted at |

### Create a Vehicle Type

This API is used to add new vehicle types to the Amitruck 2.0 platform. 

* URL: `v2/vehicle-types/create`
* Http Method: `POST`
* Content-Type: `application/json`

### List Vehicle Types

This API returns a collection of all Amitruck 2.0 vehicle types.

* URL: `v2/vehicle-types`
* Http Method: `GET`

### Retrieve a Vehicle Type

This endpoint retrieves details of an existing vehicle type. You have to pass the `ID` of the vehicle type.

* URL: `v2/vehicle-types/{ID}`
* Http Method: `GET`

