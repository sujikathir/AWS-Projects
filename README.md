
## AWS S3 Project: Working with S3 Buckets and Data Files

This README provides detailed instructions on how to create an S3 bucket, upload raw data files, query data with S3 Select, and change properties like encryption and storage type. Follow these steps to replicate the setup and operations.

### Prerequisites
* AWS account
* AWS Management Console access

*Steps to Create and Configure an S3 Bucket

![](https://github.com/sujikathir/AWS-Projects/blob/main/s3/images/s3%20home.png)

1. Create an S3 Bucket

- Navigate to S3 in the AWS Management Console.
- Click on the "Create bucket" button on the right side.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/create%20bucket.png)
  
- Enter a name for your S3 bucket using the format <id>myawsticketdata. Remember to use your unique ID at the end. [Review the naming rules if needed](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html).
- Select the AWS Region named "US West (Oregon) us-west-2".
- Under the Block Public Access header, clear the radio button for "Block all public access". Select the checkbox to acknowledge that by making this choice you understand the bucket will be public.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/block%20public%20access.png)
  
- Leave the Default encryption and other settings with their defaults. Click on the "Create bucket" button.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/encryption.png)

2. Upload Raw Data Files to the S3 Bucket
- Download the txt files uploaded in this folder.
- Ensure you have seven folders each containing a data file.
- Choose the bucket you created in the previous steps by clicking on the blue name of the bucket.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/file%20upload.png)

- After the bucket opens, click the "Upload" button.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/uploaded%20files.png)
  
- Monitor the file upload progress status bar.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/uploading%20progress.png)

3. Query Data with S3 Select
- Click on the "Version" tab. Check if versioning is turned on.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/events%20file.png)

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/object%20actions.png)
  
- After choosing the data file, click the "Object actions" menu and choose "Query with S3 Select".

- It will open the input and output settings. Click on the "Run SQL query" button to see the records.
- Choose the "Add SQL from templates" button.
- Choose the radio button beside SELECT COUNT * FROM s3object s. Click the "Copy SQL" button.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/sql%20query.png)

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/sql%20query%20events.png)

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/sql%20template.png)

- Replace the previous query with a paste of this copy. Click on the "Run SQL query" button.
From this query, we are viewing how many records are in the data file.


4. Change Properties of Encryption and Type of Storage
- Go to the bucket you created and click on it. Click on the "Objects" tab. Select all the previously loaded data folders/files. Click the "Actions" menu and choose "Edit server-side encryption".

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/edit%20server-side%20encryption.png)

- In the Server-side encryption settings section, click the radio button to "Enable" and then click the "Save changes" button. Click the "Close" button.
- Select all the folders, click on the "Actions" menu, and select "Edit storage class".
- Choose Intelligent-Tiering and then click on the "Save changes" button.

![](https://github.com/sujikathir/Using-AWS-S3-for-Data-Storage/blob/main/s3/images/intelligent-tiering.png)
