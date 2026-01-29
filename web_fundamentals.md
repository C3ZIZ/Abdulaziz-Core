# 📘 Web Development Fundamentals: A Comprehensive Guide

This guide covers the core building blocks of the web: **Client/Server architecture**, **HTTP**, **HTML**, and **CSS**. It is designed as a quick reference for definitions, usage patterns, and best practices.

---

## 1. The Big Picture: Client-Side vs. Server-Side

Understanding where code executes is the first step in web development.

| Feature | Client-Side (Frontend) | Server-Side (Backend) |
| :--- | :--- | :--- |
| **Definition** | Everything that happens in the user's web browser. | Everything that happens on the remote server (the machine hosting the site). |
| **Primary Role** | UI rendering, interactivity, animations, initial validation. | Database management, business logic, security, authentication. |
| **Languages** | HTML, CSS, JavaScript (Vanilla, React, Vue, etc.). | Python, PHP, Java, Node.js, Go, SQL. |
| **When to use?** | When you need immediate feedback (e.g., dropdown menus, toggles) without reloading. | When you need to save data permanently, log users in, or process payments. |
| **Example** | Checking if an email input contains an `@` symbol before submitting. | Verifying if that email address actually exists in the database. |

---

## 2. HTTP Protocol (The Language of the Web)

**HTTP (HyperText Transfer Protocol)** is how the Client and Server communicate. This process is called the **Request/Response Cycle**.

### A. HTTP Methods (The Action)
These methods tell the server *what* you want to do with the resource.

* **`GET`**: **Retrieve data.** Used when you visit a URL or search.
    * *Effect:* Should not change anything on the server.
* **`POST`**: **Send/Create data.** Used for login forms, signing up, or uploading files.
    * *Effect:* Creates a new resource on the server.
* **`PUT`**: **Update data (Full).** Replaces an entire record with new data.
* **`PATCH`**: **Update data (Partial).** Updates only specific fields (e.g., changing just a password).
* **`DELETE`**: **Remove data.** Deletes a resource from the server.

### B. Status Codes (The Result)
The server's way of telling you how the request went.

* **2xx (Success):**
    * `200 OK`: Request succeeded.
    * `201 Created`: Success, and a new resource was created (common after POST).
* **3xx (Redirection):**
    * `301 Moved Permanently`: The URL has changed forever.
* **4xx (Client Error):**
    * `400 Bad Request`: You sent invalid data.
    * `401 Unauthorized`: You need to log in.
    * `403 Forbidden`: You are logged in, but don't have permission.
    * `404 Not Found`: The resource doesn't exist.
* **5xx (Server Error):**
    * `500 Internal Server Error`: The server crashed or had a bug (not your fault).

---

## 3. HTML5 (Structure & Semantics)

**HTML (HyperText Markup Language)** provides the structure. Modern HTML focuses on **Semantics**—using the right tag for the right meaning (crucial for SEO and Accessibility).

### A. Semantic Structure
Avoid "div soup" (using `<div>` for everything). Use these instead:

```html
<header>    </header>
<nav>       </nav>
<main>      <article>   </article>
    <section>   </section>
</main>
<aside>     </aside>
<footer>    </footer>
