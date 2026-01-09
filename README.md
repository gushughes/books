# Bookshelf

Bookshelf is a **learning-focused REST API project** designed to explore modern API development while **prioritising clear, human-written API documentation**.

The project deliberately keeps its technical scope small. Its goal is not to build a production system, but to **understand how APIs work end to end**, and how to explain that behaviour clearly to other people.

Documentation is treated as a **first-class artifact**, written alongside the code rather than after it.

## Project Purpose

This project has three closely related goals:

1. Learn Python through a concrete, bounded problem domain (books)
2. Build a **simple, contract-first REST API**
3. Practice writing **clear, human-centred API documentation**

Modern tools are used where they support structure and clarity, but tooling itself is never the main subject.

## Data Source (Early Iterations)

Early versions of the project use data from **Open Library**.

Using an external data source allows the project to:
- Avoid manual data entry
- Work with realistic, imperfect data
- Focus on API behaviour, structure, and documentation

Later iterations may introduce a curated local dataset, but the API surface will remain intentionally small.

## Tooling (*add versions here*)

- **Python (Spyder IDE)** – scripting and API implementation  
- **FastAPI** – API framework, chosen for early schema visibility and OpenAPI generation  
- **Pandas & NumPy** – data loading and basic preprocessing  
- **GitHub** – version control  
- **Markdown, MkDocs & GitHub Pages** – project and API documentation  
- **Postman** – manual API exploration and example requests  

FastAPI is used not for performance or async complexity, but because it encourages **explicit API contracts** and supports a documentation-first workflow.

## Project Principles

This project follows a small set of intentional constraints:

- API contracts are defined early and kept simple
- Documentation is written alongside the code, not after
- Auto-generated documentation is supported by human-written explanations
- Examples and workflows are prioritised over completeness
- Tooling serves clarity, not the other way around

These constraints reflect current industry practice while keeping the project approachable.

## Conceptual Architecture

Although this project is intentionally small, it follows a **layered API model** to make request and response behaviour explicit.

A typical request flows through the following *conceptual* layers:

- **Client** – browser, curl, or Postman
- **API layer** – routing, input validation, request handling
- **Business logic** – rules, filtering, and behaviour
- **Data access** – querying and mapping data
- **Storage** – CSV files or a lightweight database

The response flows back through the same layers, where results are transformed, formatted, and returned as an HTTP response.

Not all layers are implemented as separate components in early versions of the project.  
They are kept **conceptually distinct** to support understanding, explanation, and documentation.

## Why Documentation Still Matters

Modern API frameworks can automatically generate:

- Endpoint lists
- Schemas
- Basic request and response examples

Automation is valuable, but it does not explain:

- Why an endpoint exists
- How multiple endpoints are meant to be used together
- What happens in edge cases
- How errors should be interpreted
- Where in the request flow a failure occurs

This project explicitly practices the distinction:

**Automation describes the surface of the API.  
Human-written documentation explains its behaviour and intent.**

## Project Process & Learning Goals

### Input
- Retrieve book metadata from Open Library
- Store normalised data in a CSV or lightweight data store
- Core fields may include:
  - `book_title`
  - `author`
  - `author_nationality`
  - `first_published`
  - `page_count`
  - `genre`
- Learn the basics of GitHub version control and project structure

### Handling
- Load data into Python using Pandas
- Inspect columns, data types, and missing values
- Perform minimal, explicit data cleaning
- Design REST-style resources such as:
  - `/books`
  - `/books/{id}`
  - `/authors`
- Implement basic API behaviour:
  - Listing and retrieving resources
  - Filtering and searching
  - Consistent error responses and status codes
- Follow readable, maintainable coding practices

Advanced concerns such as async optimisation, scaling, and deployment are intentionally deferred.

### Output
- A working **simple REST API** exposing book data
- Clear, structured **API documentation**, including:
  - Endpoint descriptions and intent
  - Parameters and query behaviour
  - Example requests and responses
  - Error cases and edge behaviour
- A GitHub Pages site generated with MkDocs to host the documentation

## How to Read This Project

This project is designed to be read **from the outside in**:

- Start with the API documentation
- Follow examples and workflows
- Refer to the code to see how behaviour is implemented
- Use the architecture model to understand where responsibilities live

The goal is not to memorise tools, but to build a mental model of how APIs behave and how they should be explained.

## License

This project is licensed under the  
[Creative Commons Attribution 4.0 International License](LICENSE).  
See the LICENSE file for details.