# Data_Source_API_Analyst_ImprovadoTest_
Homework assignment for Data Source API Analyst role at Improvado.

## Project Overview

This project was completed as part of a technical assessment for Improvado. The goal was to demonstrate my understanding of REST APIs, my ability to work with data extraction requirements, and my troubleshooting approach.

## Steps Performed

#### Step 1: Prepare & test a list of Reports

1. Understand Client Needs

    a. **Search Public Repositories**
        - Used the GitHub `/orgs/tidyverse/repositories` endpoint to retrieve metadata for all public repositories in the `tidyverse` organization.
        - Extracted fields like name, description, language, stars, and URL.

    b. **Get Commits**
        - Used the `/repos/{owner}/{repo}/commits` endpoint to fetch the most recent commits from the `tidyverse/tidyverse` repo.
        - Parsed commit SHA, author, date, message, and URL.

    c. **List Repository Contents**
    - Called `/repos/{owner}/{repo}/contents/` to view the structure of files in the root directory.

2. Research GitHub API:

    - Used GitHub’s REST API documentation and Copilot search to identify the correct endpoints and understand request logic, authentication, pagination, rate limits, and error handling..

#### Step 2: Set up a GitHub Repository

1. Create a New Repository

To create this new repository I performed this steps:
    - Accessed my GitHub account and created a new public repository.
    - Initialized with a README and cloned it locally via Git Bash.

2. Repository Structure
    - Wrote the content of README.md describing my approatch using VS Code
    - Added folders as instructed:
        - /Content: for data files and supporting documents
        - /Postman_Collection: for the Colab notebook

3. Commit Files
    - Committed the updated README.md and folder structure using VS Code and Git.

#### Step 3: Create a Postman Collection or Google Colab Norebook for API Extraction

1. Set Up Google Colab
     - Created a Colab notebook to write Python code for all API calls. 
     - Included one cell per API endpoint, handling authentication and response processing.

2. Extract Data Using API

The following CSV files were generated from API responses and can be found in the `/Content` folder:

- `tidyverse_repos.csv`: Metadata of all public repositories from the tidyverse organization
- `tidyverse_commits.csv`: Most recent commits from the `tidyverse/tidyverse` repository
- `tidyverse_contents.csv`: File structure of the root directory of the `tidyverse/tidyverse` repository

## 📓 Notebook

The full Python code for authentication, data extraction, and handling API logic is included in [`Postman_Collection/Github_API_Test.ipynb`](./GitHub_API_test.ipynb). It demonstrates:

- Auth token setup
- Requesting organization repositories
- Fetching commit data
- Listing repo contents
- Saving responses as CSV

## 💡 Reflections

Although I had used APIs before with R (e.g., TwitterR, Google Maps, Facebook), this was my first time building an API-based data pipeline in Python using the GitHub REST API. It helped solidify my understanding of RESTful principles, response structures, and practical considerations like pagination and rate limits.

This exercise also reinforced the importance of well-structured documentation, reproducible code, and clear output delivery.
