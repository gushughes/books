# Bookshelf

Bookshelf is a **learning project** for building REST APIs. The main goal is to write **clear, easy-to-understand documentation**.

The project makes **two small REST APIs**, one after the other. Each API teaches different things, but they both work with books and use the same basic structure.

## What This Project Does

This project has three goals:

1. Learn Python by working with books
2. Build **simple REST APIs**
3. Write **clear documentation that people can understand**

The aim is to understand how APIs work and how to explain them, not to build something for real use.

## The Two APIs

### API 1 – Open Library Explorer

The first API uses **Open Library data** that's been **saved locally**.

A **small sample** of Open Library data is downloaded and saved locally (as a CSV file). This data is then **cleaned by hand** before the API uses it. The API doesn't connect to Open Library directly.

This API helps you:
- Avoid typing in data by hand
- Work with real, messy data
- Learn to document an API when you **don't control the data**
- Focus on how the API works

This stage is about **reading, filtering, and showing external data**.

---

### API 2 – Personal Library API

The second API works with a **personal book collection**.

This API:
- Uses data you control (CSV or simple database)
- Keeps the same basic structure
- Gives you full control over the data

This stage helps you:
- Design an API when you **own the data**
- Add stricter rules
- Show that APIs can stay the same even when the data source changes
- Compare working with external data versus your own data

Together, the two APIs show the difference between **using external data** and **designing your own API**.

## Tools Used

*Add versions here*

- **Python (Spyder IDE)** – writing code  
- **FastAPI** – API framework  
- **Pandas & NumPy** – working with data  
- **GitHub** – version control  
- **Markdown, MkDocs & GitHub Pages** – documentation  
- **Postman** – testing the API  

FastAPI is used because it supports **clear API contracts** and helps with documentation.

## Project Rules

This project follows simple rules:

- Define the API early and keep it simple
- Write documentation at the same time as code
- Use auto-generated documentation plus human explanations
- Focus on examples and real use
- Tools should make things clearer

## How the APIs Are Organised

Both APIs follow the same **layered structure**.

A request goes through these layers:

- **Client** – browser, curl, or Postman
- **API layer** – routing and checking inputs
- **Business logic** – filtering and rules
- **Data access** – getting data
- **Data source** – the actual data

The response comes back through the same layers and is sent as an HTTP response.

Not all layers are separate parts in early versions. They're kept separate in concept to make things clearer.

## Why Documentation Matters

Modern frameworks can automatically create:
- Lists of endpoints
- Schemas
- Basic examples

But automation doesn't explain:
- Why endpoints exist
- How to use them together
- How edge cases work
- Where things might fail

This project practises the difference between:
- **Generated documentation**
- **Human-written explanations**

## Project Steps

### Input

- API 1: Load cleaned Open Library data
- API 2: Load personal library data
- Core fields include:
  - `book_title`
  - `author`
  - `author_nationality`
  - `first_published`
  - `page_count`
  - `genre`

### Work Done

- Look at data structure and quality
- Clean data (minimal, clear steps)
- Design REST resources like:
  - `/books`
  - `/books/{id}`
  - `/authors`
- Add:
  - Listing and getting individual items
  - Filtering and search
  - Consistent error handling
- Write readable, maintainable code

Advanced topics (async, scaling, deployment) are left for later.

### Output

- Two working, deliberately small REST APIs
- Clear, structured documentation for each API
- A GitHub Pages site made with MkDocs

## How to Read This Project

Read this project **from the outside in**:

- Start with the documentation
- Follow example requests
- Use the architecture model to understand how it works
- Look at the code to see how it's built

The goal is to understand how APIs work and how to explain them.

## Licence

This project uses the [Creative Commons Attribution 4.0 International Licence](LICENSE).

See the LICENCE file for details.
