# Backend API Documentation

## Users Endpoint

### Register Endpoint

#### **Description**
The `/users/register` endpoint is used to create a new user account.

---

### **Status Codes**
- **201 Created**: User account created successfully.
- **400 Bad Request**: Validation errors in the request data.

---

### **Request Data**

The request body must be in JSON format and contain the following fields:

- **fullname**: An object containing the user's full name.
  - **firstname**: (string) The user's first name, minimum 3 characters.
  - **lastname**: (string) The user's last name, minimum 3 characters.
- **email**: (string) The user's email address. This must be unique.
- **password**: (string) The user's password, minimum 5 characters.

### **Example Response**

- ``user`` (object): An object containing the user's full name.
    - ``fullname``: (object)
        - ``firstname``: (string) The user's last name, minimum 3 characters.
        - ``lastname``: (string) The user's last name, minimum 3 characters.
    - ``email``: (string) The user's email address. This must be unique.
    - ``password``: (string) The user's password, minimum 5 characters.
- ``token`` (String): JWT Token.

#### **Example Request Data**
```json
{
  "fullname": {
    "firstname": "John",
    "lastname": "Doe"
  },
  "email": "john.doe@example.com",
  "password": "password123"
}
