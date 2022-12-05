## VEHICLE BODY TYPE

### CREATE A VEHICLE BODY TYPE
> REQUEST
```json
{
    "name": "vehicle body type Name",
    "description": "vehicle body type Description"
}
```

> RESPONSE
```json
{
    "code": 201,
    "status": "success",
    "message": "Truck vehicle body type was added",
    "data": [
        {
            "id": 1,
            "name": "Truck",
            "slug": "truck",
            "description": "Vehicle that can transport 5T",
            "created_at": "2022-12-01T08: 12: 22.049585Z",
            "updated_at": "2022-12-01T08: 12: 22.049585Z",
            "deleted_at": null
        }
    ]
}
```

This endpoint creates a new vehicle body type to the platform.
- URL: `v2/vehicles/body/types/create`
- METHOD: `POST`
- CONTENT-TYPE: `application/json`

### LIST VEHICLE BODY TYPES

> LIST RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "vehicle body types retrieved successfully",
    "data": [
        {
            "id": 1,
            "name": "Gary Schneider",
            "slug": "gary-schneider",
            "description": "Represent kitchen I water present",
            "created_at": "2022-12-01T08:24:32.605194Z",
            "updated_at": "2022-12-01T08:24:32.605194Z",
            "deleted_at": null
        },
        {
            "id": 2,
            "name": "Erica Rose",
            "slug": "eric-rose",
            "description": "Police number focus foot test.",
            "created_at": "2022-12-01T08:24:32.605194Z",
            "updated_at": "2022-12-01T08:24:32.605194Z",
            "deleted_at": null
        }
    ]
}
```

Retrieves all registered vehicle body types from Amitruck 2.0
- URL: `v2/vehicles/body/types`
- METHOD: `GET`

### RETRIEVES A SINGLE VEHICLE BODY TYPE

> RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "Truck vehicle body type was added",
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

Retrieves a single vehicle body type by its resource ID.

- URL: `v2/vehicles/body/types/{ID}`
- METHOD: `GET`

### UPDATE A VEHICLE BODY TYPE

> REQUEST
```json
{
    "name": "Body type Name Updated",
    "slug": "name-updated"
    "description": "Description Updated"
}
```

> RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "vehicle body type successfully updated",
    "data": [
        {
            "id": 1,
            "name": "Body type Name Updated.",
            "slug": "body-type-name-updated",
            "description": "Description Updated",
            "created_at": "2022-12-01T08:28:14.683819Z",
            "updated_at": "2022-12-01T08:28:14.687819Z",
            "deleted_at": null
        }
    ]
}
```

- URL: `v2/vehicles/body/types/{ID}/update`
- METHOD: `PUT`
- CONTENT-TYPE: `application/json`

### DELETE A VEHICLE BODY TYPE

> DELETE RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "vehicle body type delete successful."
}
```

Soft delete an existing vehicle body type. The deleted vehicle type can be restored later on if needed, hence, the need for the soft delete.

- URL: `v2/vehicles/body/types/{ID}/delete`
- METHOD: `DELETE`
- CONTENT-TYPE: `application/json`



### RESTORE A DELETED VEHICLE BODY TYPE
> REQUEST: `v2/vehicles/body/types/{ID}/restore`

> RESPONSE

```json
{
    "code": 200,
    "status": "success",
    "message": "vehicle body type restored.",
    "data": [
        {
            "id": 2,
            "name": "Name Updated.",
            "description": "Description Updated",
            "created_at": "2022-12-01T08:28:14.683819Z",
            "updated_at": "2022-12-01T08:28:14.687819Z",
            "deleted_at": null
        }
    ]
}
```
This API makes it possible to restore a soft-deleted vehicle body type by passing the deleted vehicle body type ID as a parameter.
