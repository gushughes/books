# Bookshelf

Bookshelf is a **learning-focused REST API project** designed to explore modern API development while **prioritising clear, human-written API documentation**.

The project is intentionally structured around **two small REST APIs**, built in sequence. Each API serves a distinct learning purpose while sharing the same conceptual model, structure, and documentation principles.

## Project Purpose

This project has three closely related goals:

1. Learn Python through a concrete, bounded problem domain (books)
2. Build **simple, contract-first REST APIs**
3. Practice writing **clear, human-centred API documentation**

The emphasis is on understanding API behaviour, structure, and explanation rather than building a production system.

## Project Structure: Two APIs

### API 1 — Open Library Explorer

The first REST API is built on top of **Open Library data**, treated as an **external but locally stored dataset**.

For learning purposes, a **small, representative subset** of Open Library data is downloaded and stored locally (for example as a CSV file). This dataset is then **manually cleaned and normalised** before being used by the API. The API does not make live calls to Open Library.

This API exists to:
- Avoid manual data entry
- Work with realistic, imperfect external data
- Practice documenting behaviour when you **do not own the data**
- Focus on API contracts, behaviour, and documentation patterns

This stage emphasises **reading, filtering, and presenting external data clearly**.

---

### API 2 — Personal Library API

The second REST API is built around a **curated personal book collection**.

This API:
- Uses locally controlled data (CSV or lightweight database)
- Preserves the same conceptual API structure
- Allows full control over schema, validation, and behaviour

This stage exists to:
- Practice API design when you **own the data**
- Introduce stricter validation and consistency
- Demonstrate that API behaviour can remain stable while data sources change
- Contrast first-party API design with external data integration

Together, the two APIs illustrate the difference between **wrapping external data** and **designing a first-party API**.

## Tooling (*add versions here*)

- **Python (Spyder IDE)** – scripting and API implementation  
- **FastAPI** – API framework, chosen for early schema visibility and OpenAPI generation  
- **Pandas & NumPy** – data loading and preprocessing  
- **GitHub** – version control  
- **Markdown, MkDocs & GitHub Pages** – project and API documentation  
- **Postman** – manual API exploration and example requests  

FastAPI is used to support **explicit API contracts** and a documentation-first workflow, not for async performance or deployment complexity.

## Project Principles

This project follows a small set of intentional constraints:

- API contracts are defined early and kept simple
- Documentation is written alongside the code, not after
- Auto-generated documentation is supported by human-written explanations
- Examples and workflows are prioritised over completeness
- Tooling serves clarity, not the other way around

## Conceptual Architecture

Although the project is intentionally small, both APIs follow the same **layered conceptual model**.

A typical request flows through these conceptual layers:

- **Client** – browser, curl, or Postman
- **API layer** – routing, input validation, request handling
- **Business logic** – filtering, rules, and behaviour
- **Data access** – querying and mapping data
- **Data source** – local Open Library dataset or personal library data

The response flows back through the same layers, where results are transformed, formatted, and returned as an HTTP response.

Not all layers are implemented as separate components in early versions.  
They are kept conceptually distinct to support clarity and documentation.

## Why Documentation Still Matters

Modern frameworks can automatically generate:
- Endpoint lists
- Schemas
- Basic request and response examples

Automation describes the *surface* of an API, but it does not explain:
- Why endpoints exist
- How they are intended to be used together
- How edge cases are handled
- Where failures occur in the request flow

This project explicitly practices the distinction between:
- **Generated reference documentation**
- **Human-written explanations of behaviour and intent**

## Project Process & Learning Goals

### Input
- API 1: Load and reshape a cleaned, local subset of Open Library data
- API 2: Load curated personal library data
- Core fields may include:
  - `book_title`
  - `author`
  - `author_nationality`
  - `first_published`
  - `page_count`
  - `genre`

### Handling
- Inspect data structure and quality
- Perform minimal, explicit data cleaning
- Design REST-style resources such as:
  - `/books`
  - `/books/{id}`
  - `/authors`
- Implement:
  - Listing and retrieval
  - Filtering and search
  - Consistent error handling and status codes
- Follow readable, maintainable coding practices

Advanced concerns (async optimisation, scaling, deployment) are intentionally deferred.

### Output
- Two working, intentionally small REST APIs
- Clear, structured API documentation for each API
- A GitHub Pages site generated with MkDocs

## How to Read This Project

This project is designed to be read **from the outside in**:

- Start with the documentation
- Follow example requests and workflows
- Use the architecture model to understand behaviour
- Refer to the code to see how responsibilities are implemented

The goal is to build a mental model of how APIs behave and how they should be explained.

## License

This project is licensed under the  
[Creative Commons Attribution 4.0 International License](LICENSE).  
See the LICENSE file for details.