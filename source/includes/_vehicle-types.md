## Vehicle Types
The vehicle types service allows you to add a new vehicle type in terms of the Trucks, Tuktuk, Bikes, Van or any other vehicle types.
These types are listed on during the vehicle registration page and the vehicle services depend on it. 

This service requires authentication.

### Vehicle Type Properties

| Attribute | Type | Description |
| ----------- | ----------- |
| id  | Integer | Unique identifier of the resource `readonly` |
| name | string | Vehicle type name |
| description | string | Vehicle type description |
| created_at | date-time | Vehicle type created at |
| updated_at | date-time | Vehicle type updated at |
| deleted_at | date-time | Vehicle type deleted at |

### Create a Vehicle Type
This API is used to add new vehicle types to the Amitruck 2.0 platform. 

* URL: `v2/vehicles/create`
* Http Method: `POST`
* Content-Type: `application/json`

> Create a vehicle type request:

```json
{
    "name": "Vehicle Type Name",
    "description": "Vehicle Type Description"
}
```

> Response

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
