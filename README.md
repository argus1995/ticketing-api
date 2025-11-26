# Ticketing System API

A simple Ticketing System REST API built with Laravel, designed as an
MVP to demonstrate skills in: - Laravel framework - REST API design -
MySQL - Authentication - Ticket &
Comment workflow

------------------------------------------------------------------------

## 🚀 Features (MVP)

### 1. **Authentication**

-   Register
-   Login (Sanctum)
-   Logout
-   Protected routes

### 2. **Tickets**

-   Create a ticket
-   View all tickets
-   View single ticket
-   Update ticket (status, title, description)
-   Delete ticket

### 3. **Comments**

-   Add comment to a ticket
-   View comments for a ticket

------------------------------------------------------------------------

## 🧱 Tech Stack

-   **Laravel 12**
-   **MySQL**
-   **Laravel Sanctum** (recommended)
-   **Eloquent ORM**
-   **REST API structure**

------------------------------------------------------------------------

## 📦 Installation

``` bash
git clone https://github.com/yourusername/ticketing-api.git
cd ticketing-api
composer install
cp .env.example .env
php artisan key:generate
```

Set your database credentials in `.env`.

Run migrations:

``` bash
php artisan migrate
```

Start server:

``` bash
php artisan serve
```

------------------------------------------------------------------------

## 🔑 Authentication Endpoints

| Method | Endpoint       | Description    |
|--------|----------------|----------------|
| POST   | /api/register  | Register user  |
| POST   | /api/login     | Login user     |
| POST   | /api/logout    | Logout user    |

------------------------------------------------------------------------

## 🎫 Ticket Endpoints

  | Method   | Endpoint                | Description       | 
  | -------- | ----------------------- | ----------------- | 
  | GET      | /api/tickets            | Get all tickets   | 
  | GET      | /api/tickets/{ticket}   | Get one ticket    | 
  | POST     | /api/tickets            | Create ticket     | 
  | PATCH    | /api/tickets/{ticket}   | Update ticket     | 
  | DELETE   | /api/tickets/{ticket}   | Delete ticket     | 

------------------------------------------------------------------------

## 💬 Comment Endpoints

 | Method   | Endpoint                         | Description                | 
 | -------- | -------------------------------- | -------------------------- | 
 | POST     | /api/tickets/{ticket}/comments   | Add a comment              | 
 | GET      | /api/tickets/{ticket}/comments   | List comments for ticket   | 

------------------------------------------------------------------------

## 📘 Example Ticket Payload

``` json
{
  "title": "Printer not working",
  "description": "The main office printer is offline.",
  "priority": "high"
}
```

------------------------------------------------------------------------

## 📘 Example Comment Payload

``` json
{
  "message": "Checked printer, restarting now."
}
```

------------------------------------------------------------------------

## 📐 Database Structure

### **Users**

-   id
-   name
-   email
-   password

### **Tickets**

-   id
-   user_id
-   title
-   description
-   status (open, in_progress, resolved)
-   priority (low, medium, high)

### **Comments**

-   id
-   ticket_id
-   user_id
-   message

------------------------------------------------------------------------

## ✔ Status Flow

    open → in_progress → resolved

------------------------------------------------------------------------

## 🏁 Future Improvements

-   File attachments
-   Ticket categories
-   Admin dashboard
-   Email notifications
-   SLA monitoring

------------------------------------------------------------------------

## 📄 License

MIT License
