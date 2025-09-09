# TryHackMe Notes: HTTP in Detail

## What is HTTP?

- **HTTP (HyperText Transfer Protocol):** Rules for communication between client (browser) and server.
- Created by **Tim Berners-Lee (1989–1991)**.
- Transfers data like HTML, images, videos, etc.

## What is HTTPS?

- **HTTPS (HTTP Secure):** Encrypted version of HTTP using **TLS/SSL**.
- Ensures **confidentiality**, **integrity**, and **authenticity** of data.

---

## Common HTTP Methods

- **GET** → Retrieve information from server.
- **POST** → Submit data (create new records).
- **PUT** → Update existing information.
- **DELETE** → Remove data from server.
- **HEAD** → Same as GET but only retrieves headers (no body).

---

## HTTP Status Codes

**1xx – Informational**

- 100 Continue → Request part accepted, continue sending.

**2xx – Success**

- 200 OK → Request successful.
- 201 Created → New resource created.

**3xx – Redirection**

- 301 Moved Permanently → Resource moved.
- 302 Found → Temporary redirect.
- 307 Temporary Redirect → Similar to 302 but method must not change.

**4xx – Client Errors**

- 400 Bad Request → Invalid request.
- 401 Unauthorized → Need authentication.
- 403 Forbidden → No permission.
- 404 Not Found → Resource doesn’t exist.
- 405 Method Not Allowed → Wrong HTTP method used.

**5xx – Server Errors**

- 500 Internal Server Error → Generic server error.
- 503 Service Unavailable → Overloaded or maintenance.

---

## Common Request Headers

- **Host:** Specifies target domain (useful for virtual hosting).
- **User-Agent:** Browser & version info.
- **Content-Length:** Size of data being sent.
- **Accept-Encoding:** Compression methods supported.
- **Cookie:** Sends stored cookies to server.

## Common Response Headers

- **Set-Cookie:** Server tells browser to store a cookie.
- **Cache-Control:** Defines how long content can be cached.
- **Content-Type:** Type of data (HTML, JSON, image, etc.).
- **Content-Encoding:** Compression method used.

---

## Cookies

- Small pieces of data stored on client.
- Sent by server with **Set-Cookie** header.
- Returned to server in subsequent requests via **Cookie** header.

---

## Key Takeaways

- **HTTP vs HTTPS:** HTTPS adds encryption (TLS/SSL).
- **Most used methods:** GET & POST.
- **Most common errors:** 404 (Not Found), 403 (Forbidden), 500 (Server Error).
- **Headers matter:** Help client & server exchange context (cookies, caching, compression).
