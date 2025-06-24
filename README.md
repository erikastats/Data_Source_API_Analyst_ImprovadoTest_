# Data_Source_API_Analyst_ImprovadoTest_
Homework assignment for Data Source API Analyst role.

## Project Overview

This project was completed as part of a Data Source API Analyst Homework for the company Improvado. Teh goal was to assess my understanding of APIs, my ability to work with data extraction requirements, and my troubleshooting approach.

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

I used the search copilot on the Github REST API documentation to help me identify the endpoints to cover the client's needs, Requests Logic, Pagination, Rate limits, Error Handling, etc.

#### Step 2: Set up a GitHub Repository

1. Create a New Repository

To create this new repository I performed this steps:
    - Accessed my GitHub account 
    - Went to New
    - Set the repository as Public
    - Created a README.md file and launched
    - Went to the git bash on my computer and clone the repository using `git clone repository_path`

2. Repository Structure
    - Wrote the content of README.md describing my approatch using VS Code
    - Added new folders as requested (Content, Postman_Collection)

3. Commit Files
    - Commited the new information on README.md and the folder estructure using VS Code to commit the changes.

#### Step 3: Create a Postman Collection or Google Colab Norebook for API Extraction

1. Set Up Postman or Google Colab
     - I created a new notebook on Google Colab
     - Used the endpoints for each request
     - Included a cell for each API endpoint I was testing
2. Extract Data Using API

The following CSV files were generated from API responses and can be found in the `/Content` folder:

- `tidyverse_repos.csv`: Metadata of all public repositories from the tidyverse organization
- `tidyverse_commits.csv`: Most recent commits from the `tidyverse/tidyverse` repository
- `tidyverse_contents.csv`: File structure of the root directory of the `tidyverse/tidyverse` repository