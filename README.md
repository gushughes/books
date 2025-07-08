# Bookshelf

I’m learning Python by working with data from a small home book collection and using tools to organize, analyze and document it.

## Research Question

This project looks at whether authors’ publication dates show any real patterns or are just spread out randomly. It uses simple tools to analyze the book data and spot any trends in when authors published.

## Tools (*add versions here)

- LibreOffice Calc – storing & data handling  
- Python & JupyterLab – data analysis
- GitHub – version control  
- Markdown & MkDocs – documentation  

I hope to contribute to open source GitHub projects in the future.

## Project Process & Learning Goals

### Input
- Collate data into a CSV file ('entries') with these columns:
  - `book_title`
  - `author`
  - `author_nationality`
  - `first_published`
  - `page_count`
  - `genre`
- Learn the basics of GitHub version control

### Handling
- Learn to use Python libraries (Pandas, NumPy, Matplotlib, Seaborn) for basic exploratory data analysis (EDA)
- Load the CSV into a Pandas DataFrame (data structure: dictionary)
- Check columns, data types, and handle missing values
- Perform data cleaning and preprocessing (explore variable types, string formatting)
- Apply analysis techniques (algorithms or functions) to extract insights such as:
  - **book_title:** Search by title, count duplicates, keyword analysis
  - **author:** Grouping authors and identifying most prolific authors
  - **first_published:** Analyze time trends, earliest/latest books amd historical filters
  - **page_count:** Calculate average, minimum, maximum page counts; filter by size
  - **author_nationality:** Diversity analysis and regional trends
  - **genre:** Identify popular genres, multi-genre grouping and filtering
- Clean or transform data as needed
- Follow PEP 8 and other best practices throughout the process

### Output
- Test the hypothesis by identifying and explaining significant descriptive statistics (if any) in publication dates
- Test the hypothesis by identifying and explaining significant visual patterns (if any) in publication dates
- Create a GitHub Pages site for documentation using MkDocs

- ## License
This project is licensed under a [Creative Commons Attribution 4.0 International License](LICENSE). See the LICENSE file for details.
