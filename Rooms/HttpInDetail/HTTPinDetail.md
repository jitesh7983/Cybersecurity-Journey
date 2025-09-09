# TryHackMe: HTTP in Detail

**Room Link:** [HTTP in Detail - TryHackMe](https://tryhackme.com/room/httpindetail)  
**Difficulty:** Easy  
**Category:** Pre-Security  
**Completion Date:** Sept 8, 2025

---

## Overview

This room gave me a clear understanding of the **HyperText Transfer Protocol (HTTP)** and its secure version (**HTTPS**). I learned about request methods, status codes, headers, and how to interact with HTTP servers practically using GET, POST, PUT, and DELETE requests.

---

## Key Learnings

- **HTTP vs HTTPS:**

  - HTTP: Protocol for communication between client and server (unencrypted).
  - HTTPS: Encrypted with TLS/SSL, ensures security and authenticity.

- **HTTP Methods:**

  - **GET:** Retrieve data from a server.
  - **POST:** Send data to create a resource.
  - **PUT:** Update an existing resource.
  - **DELETE:** Remove a resource.

- **Status Codes:**

  - **2xx:** Success (200 OK, 201 Created).
  - **3xx:** Redirection (301 Moved Permanently, 302 Found).
  - **4xx:** Client errors (400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found).
  - **5xx:** Server errors (500 Internal Server Error, 503 Service Unavailable).

- **Headers:**

  - **Request Headers:** Host, User-Agent, Content-Length, Accept-Encoding, Cookie.
  - **Response Headers:** Set-Cookie, Cache-Control, Content-Type, Content-Encoding.

- **Cookies:** Small pieces of data stored on the client and sent with each request, used for session management and personalization.

---

## Practical Tasks and Flags

| Task                                                                      | Request          | Flag                      |
| ------------------------------------------------------------------------- | ---------------- | ------------------------- |
| Make a GET request to `/room`                                             | `GET /room`      | `THM{YOU'RE_IN_THE_ROOM}` |
| Make a GET request to `/blog` with parameter `id=1`                       | `GET /blog?id=1` | `THM{YOU_FOUND_THE_BLOG}` |
| Make a DELETE request to `/user/1`                                        | `DELETE /user/1` | `THM{USER_IS_DELETED}`    |
| Make a PUT request to `/user/2` with body `username=admin`                | `PUT /user/2`    | `THM{USER_HAS_UPDATED}`   |
| Make a POST request to `/login` with body `username=thm&password=letmein` | `POST /login`    | `THM{USER_HAS_UPDATED}`   |

---

### Example Requests

```http
# GET request
GET /room HTTP/1.1
Host: website.thm

# GET request with parameter
GET /blog?id=1 HTTP/1.1
Host: website.thm

# DELETE request
DELETE /user/1 HTTP/1.1
Host: website.thm

# PUT request
PUT /user/2 HTTP/1.1
Host: website.thm
Content-Type: application/x-www-form-urlencoded
Content-Length: 15

username=admin

# POST request
POST /login HTTP/1.1
Host: website.thm
Content-Type: application/x-www-form-urlencoded
Content-Length: 25

username=thm&password=letmein
```

# completion proof

![Completion Image](images/HTTPindetail.png)
