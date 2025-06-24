# 🧹 Data Cleaning & Structuring Approach

## 1. Repositories Data
- Called `/orgs/tidyverse/repos` to get all public repos.
- Selected relevant fields: `name`, `full_name`, `description`, `language`, `stars`, `url`, etc.
- Converted the JSON response to a pandas DataFrame and saved it as CSV.

## 2. Commits Data
- Called `/repos/tidyverse/tidyverse/commits`.
- Extracted only the latest 50 commits for demonstration.
- Flattened the nested JSON to extract: `sha`, `author`, `date`, `message`, `html_url`.

## 3. Contents Data
- Called `/repos/tidyverse/tidyverse/contents/`.
- Parsed file metadata like: `name`, `type`, `size`, `download_url`.
- Converted to a DataFrame and saved as CSV.

## 4. General Notes
- Removed nested or unused fields to simplify the data.
- Handled potential null fields gracefully using `.get()` or conditional checks.
