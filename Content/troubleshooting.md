# 🛠 Troubleshooting Guide

## 1. 404 - Not Found (Invalid Path)
**Issue**: Received a 404 error when trying to retrieve repo contents.  
**Cause**: The `path` provided in the endpoint did not exist.  
**Solution**: Called `/contents/` to list the root files, then updated the path based on what actually exists.

## 2. 401 - Unauthorized (Token missing or invalid)
**Issue**: API requests failed with a 401 error.  
**Cause**: Missing or expired GitHub token, or incorrect authorization format.  
**Solution**: Generated a new personal access token and added it using Bearer authentication in the headers:
```python
"Authorization": f"Bearer {token}"


