---
sidebar_position: 6
sidebar_label: API
tags:
  - file-upload
  - API
---

# File uploading API
Manage file uploading, retrieving files after uploading.

## Uploading a file to server  
This is the API for uploading a single file for each request, using HTTP with multipart/form-data to upload file.

### Request 
`POST /files/upload`  

**Request body (Form data)**: 
```
file: "multipart/form-data"
```

### Response   
```json 
{
    "originalname": "commercial_invoice.png",
    "encoding": "7bit",
    "mimetype": "image/png",
    "destination": "tmp/upload/origin",
    "filename": "6763fa8f0d9b2248416dd492",
    "path": "tmp/upload/origin/6763fa8f0d9b2248416dd492",
    "_id": "6763fa8f0d9b2248416dd493", // Id to retrieve the file after uploading
    "createdAt": "2024-12-19T10:50:55.990Z",
    "updatedAt": "2024-12-19T10:50:55.990Z",
    "__v": 0
}
```

## Retrieve file
This is the API for retrieving the file after uploading. It will use **width** and **height** to determine the appropriate image resolution to send to client so it is more efficient than load a large image.

### Request 
`GET /files/:id?width=100&height=100`  

**Query**:
- **width**: width of the frame that you're going to load the image into
- **height**: height of the frame that you're going to load the image into

### Response   
The image which was be requested.