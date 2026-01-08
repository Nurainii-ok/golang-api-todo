# Golang Todo API

## Deskripsi
Golang Todo API adalah REST API sederhana untuk mengelola data Todo List.  
API ini menyediakan fitur CRUD (Create, Read, Update, Delete) dan mengembalikan response dalam format JSON.

## Cara Menjalankan Project
1. Pastikan Golang sudah terinstall
2. Jalankan perintah berikut di terminal:
    ```bash
    go run main.go
    Server akan berjalan di:
    http://localhost:8080

## Endpoint API
1. Create todo
    Method : Post
    Endpoint : /todos
    Request :
                {
                    "title": "Belajar Golang",
                    "description": "Todo pertama saya"
                }
    Response : 
                {
                    "id": 1,
                    "title": "Belajar Golang",
                    "description": "Todo pertama saya",
                    "status": "pending",
                    "created_at": "2026-01-08T09:57:04+07:00"
                }

2. Get list todo
    Method : GET
    Endpoint : /todos
    Response :
                [
                    {
                        "id": 1,
                        "title": "Belajar Golang",
                        "description": "Todo pertama saya",
                        "status": "pending",
                        "created_at": "2026-01-08T09:57:04+07:00"
                    }
                ]

3. Get detail todo
    Method : GET
    Endpoint : /todos/{id}
    contoh : /todos/1
    Response : 
                {
                    "id": 1,
                    "title": "Belajar Golang",
                    "description": "Todo pertama saya",
                    "status": "pending",
                    "created_at": "2026-01-08T09:57:04+07:00"
                }

4. Update todo
    Method : PUT
    Endpoint : /todos/{id}
    Request :
                {
                    "title": "Belajar Golang Update",
                    "description": "Todo sudah diupdate",
                    "status": "done"
                }

    Response :
                {
                    "id": 1,
                    "title": "Belajar Golang Update",
                    "description": "Todo sudah diupdate",
                    "status": "done",
                    "created_at": "2026-01-08T09:57:04+07:00"
                }

5. Delete todo
    Method: DELETE
    Endpoint: /todos/{id}
    Response :
                {
                    "message": "Todo deleted"
                }

