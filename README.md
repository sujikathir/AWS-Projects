# AWS
Services: S3, Athena, Redshift, Glue, Quicksight, Sagemaker, IoT, Kinesis

## AWS S3 Project: Working with S3 Buckets and Data Files

This README provides detailed instructions on how to create an S3 bucket, upload raw data files, query data with S3 Select, and change properties like encryption and storage type. Follow these steps to replicate the setup and operations.

### Prerequisites
* AWS account
* AWS Management Console access

*Steps to Create and Configure an S3 Bucket

1. Create an S3 Bucket
- Navigate to S3 in the AWS Management Console.
- Click on the "Create bucket" button on the right side.
- Enter a name for your S3 bucket using the format <id>myawsticketdata. Remember to use your unique ID at the end. Review the naming rules if needed.
- Select the AWS Region named "US West (Oregon) us-west-2".
- Under the Block Public Access header, clear the radio button for "Block all public access". Select the checkbox to acknowledge that by making this choice you understand the bucket will be public.
- Leave the Default encryption and other settings with their defaults. Click on the "Create bucket" button.

2. Upload Raw Data Files to the S3 Bucket
- Download the tickitdb.zip file from eLearning.
- Ensure you have seven folders each containing a data file.
- If the extract did not create folders, create a folder for each data file and insert the data file into the respective folder that matches the name of the data file.
- Choose the bucket you created in the previous steps by clicking on the blue name of the bucket.
- After the bucket opens, click the "Upload" button.
- Click the "Add folder" button to create a folder for the data file. Navigate to the location where you extracted/saved the data files on your laptop. Select the folder you wish to upload, and then select "Upload". Upload all the folders that you extracted in the previous step.
- Monitor the file upload progress status bar.

3. Query Data with S3 Select
- Click on the "Version" tab. Check if versioning is turned on.
- After choosing the data file, click the "Object actions" menu and choose "Query with S3 Select".
- It will open the input and output settings. Click on the "Run SQL query" button to see the records.
- Choose the "Add SQL from templates" button.
- Choose the radio button beside SELECT COUNT * FROM s3object s. Click the "Copy SQL" button.
- Replace the previous query with a paste of this copy. Click on the "Run SQL query" button.
- Take a screenshot of your query results. Ensure the date/time stamp from the menu bar of your laptop is included.

4. Change Properties of Encryption and Type of Storage
- Go to the bucket you created and click on it. Click on the "Objects" tab. Select all the previously loaded data folders/files. Click the "Actions" menu and choose "Edit server-side encryption".
- In the Server-side encryption settings section, click the radio button to "Enable" and then click the "Save changes" button. Click the "Close" button.
- Select all the folders, click on the "Actions" menu, and select "Edit storage class".
- Choose Intelligent-Tiering and then click on the "Save changes" button.
