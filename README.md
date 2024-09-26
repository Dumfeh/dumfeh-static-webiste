AWS S3 Static Website Project

Project Overview
This project demonstrates how to host a static website using Amazon S3. The website showcases my journey from a non-technical background to acquiring skills in Cloud Engineering, with support from Azubi Africa. It includes a brief story about my career development, a motivational quote, and a "Hello World!" message to mark the beginning of my cloud journey.

Project Objectives
Host a static website on AWS S3.
Create a custom HTML/CSS page that tells my story of transitioning into cloud computing.
Configure the S3 bucket for static website hosting.
Set public access permissions via a bucket policy to allow everyone to view the website.
Technologies Used
Amazon S3 (Simple Storage Service)
HTML5 for content structure
CSS3 for styling
Project Setup
Prerequisites
To complete this project, you need:

An AWS Account.
Basic knowledge of HTML and CSS.
The following files:
index.html: Main content of the website.
styles.css: Stylesheet for the website.
Steps to Set Up
Create an S3 Bucket:

Log in to the AWS Management Console and navigate to S3.
Click Create bucket and provide a globally unique name.
Leave the remaining options at their default and click Create bucket.
Enable Static Website Hosting:

Open your S3 bucket and go to the Properties tab.
Scroll down to Static website hosting and click Edit.
Select Enable and set the index document to index.html.
Save changes.
Upload Files to S3:

In the Objects tab of your S3 bucket, click Upload.
Upload index.html and styles.css.
Ensure both files are uploaded successfully.
Set Bucket Policy for Public Access:

Go to the Permissions tab of the bucket.
Scroll down to the Bucket Policy section.
Add the following policy (replace your-bucket-name with your bucket's name):
json
Copy code
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
Save the policy.
Test Your Static Website:

After the bucket is publicly accessible, your static website can be accessed through the S3 bucket website URL provided in the Static website hosting section under the Properties tab.
