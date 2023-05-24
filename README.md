# Lambda Function - docxtopdf

This repository contains a Lambda function that provides an API endpoint to upload Word files (docx) to an S3 bucket. The function accepts HTTP POST requests with the file content and saves the file to the specified S3 bucket. It also generates a unique file name using the current timestamp.

## hosted on : https://filehosting-index.s3.us-east-2.amazonaws.com/index.html
## Setup

1. Create an S3 bucket to store the uploaded files. Note down the bucket name for configuration.

2. Configure the Lambda function with the following settings:
   - Runtime: Python 3.x
   - Handler: lambda_function.lambda_handler
   - Execution Role: Ensure the role has permissions to write objects to the S3 bucket.

3. Copy the code from the Lambda function (`lambda_function.py`) and paste it into your Lambda function code editor.

4. Modify the following variables in the code:
   - `bucket_name`: Replace with your S3 bucket name.
   - `s3_subfolder`: Specify the subfolder within the bucket to store the files.
   - `file_upload_path`: Specify the API endpoint path for file uploads.

5. Save the Lambda function.

6. Create an API Gateway (REST API) and configure it to integrate with the Lambda function. Note down the API endpoint URL for use in the frontend.

## Frontend - index.html

The `index.html` file provides a simple user interface to upload Word files using Bootstrap. It includes file validation to ensure only Word files (docx) are accepted, with a maximum file size limit of 5MB. The frontend sends a POST request to the API endpoint with the selected file for upload.

To use the frontend:

1. Copy the code from `index.html` and save it as an HTML file.

2. Open the HTML file in a web browser.

3. In the web browser, select a Word file to upload using the file input field.

4. Click the "Upload" button to initiate the file upload.

5. If the file upload is successful, a success message will be displayed. Otherwise, an error message will be shown.


