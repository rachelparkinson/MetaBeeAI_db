
---

## Data Description

The database is initialized using the `papers_dataset_domains.csv` file located in the `data` folder. This file contains the following columns:

- `record_id`: Unique identifier for each paper, used as the primary key in the database.
- `title`: Title of the paper.
- `type_of_reference`: Type of the reference (e.g., journal article, conference paper).
- `authors`: List of authors.
- `secondary_title`: Secondary title (e.g., journal name).
- `abstract`: Abstract of the paper.
- `year`: Year of publication.
- `doi`: Digital Object Identifier for the paper.
- `volume`: Volume of the journal or publication.
- `commu`, `indiv`, `letha`, `molec`, `popul`, `subin`: Domain-specific inclusion flags.
- `path`: Path to the folder containing the associated PDF and supplemental files.

---

## Setup Instructions

1. **Clone the Repository**  
   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-username/MetaBeeAI_db.git

2. **Set up a Virtual Environment**
    Create and activate a Python virtual environment:
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate

3. **Install Dependencies**
    Install the required Python packages:
    ```bash
    pip install -r requirements.txt

4. **Initialize the Database**  
   - Open the Jupyter Notebook `notebooks/setup_database.ipynb`.
   - Run the cells to create the SQLite database and populate it with data from `papers_dataset_domains.csv`.

5. **Query the Database**  
   - Use the Jupyter Notebook `notebooks/query_database.ipynb` to explore the database.
   - Execute SQL queries to retrieve and analyze data.


## Query Examples
Here are some example SQL queries you can run in the database:

**Fetch Record ID and Title**
Retrieve the record_id and title of the first 10 entries:
    ``` bash
    SELECT record_id, title FROM papers LIMIT 10;

 **Filter by Year**
 Retrieve all papers published in a specific year:
     ``` bash 
    SELECT * FROM papers WHERE year = 2020;

## Future Extensions
This project is designed to be flexible and extensible. Planned extensions include:

**Supplemental Data Management**
    - Extend the database schema to store and query supplemental files (e.g., .json, .txt, or raw data).

**LLM Integration**
    - Integrate with a large language model (LLM) to extract information from PDFs.
    - Store structured data outputs, such as text chunks or metadata, in the database.

**Data Enrichment**
    - Add additional metadata fields as required (e.g., keywords, funding sources, citations).

## Contributions

Contributions are welcome! If you'd like to improve the database or add new features, please feel free to:

1. Fork the repository.
2. Make your changes.
3. Submit a pull request.

For any issues or suggestions, feel free to open an issue in the repository.

---

## License

This project is licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.  
