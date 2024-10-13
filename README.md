# Deploying an AWS Lambda Function

### Objectives: 

- Create a Lambda function to resize an image to a thumbnail after upload. 

- Configure an S3 bucket as a Lambda event source. 

- Invoke a Lambda function by uploading an object to Amazon S3. 

- Monitor AWS Lambda S3 functions through Amazon CloudWatch Logs.

### Environment: 
![Lamda_Environment](https://github.com/user-attachments/assets/32a50015-181c-401b-a824-9bf142c3511c)

A user uploads an object to the source bucket in Amazon S3 (object-created event). Amazon S3 detects the object-created event and publishes the event to AWS Lambda by invoking the Lambda function and passing event data as a function parameter. AWS Lambda runs the Lambda function. From the event data it receives, the Lambda function knows the source bucket name and object key name. The Lambda function reads the object and creates a thumbnail using graphics libraries, then saves the thumbnail to the target bucket. 


1. Create the source S3 bucket 

2. Create the target S3 bucket 

3. Upload a picture to source S3 bucket 

![Lambda Function_HappyFace_Large](https://github.com/user-attachments/assets/c09716b2-7baa-4cad-a1bc-a662a9dcf238)


4. Create and configure a Lambda function 
 - Create Lambda function 
 - Add an Amazon S3 trigger 
 - Configure the Lambda function; upload zip file 
 

It receives an event, which contains the name of the incoming object (bucket, key). 

- It downloads the image to local storage. 
- It resizes the image using the Pillow library. 
- It uploads the resized image to the -resized bucket. 


5. Test the Lambda Function and verify output 

6. Reviewed event logs in AWS CloudWatch 

7. Image has been resized in target S3 bucket
   
![Lambda Function_HappyFace_Thumbnail](https://github.com/user-attachments/assets/3cfc9abc-5fdb-4a54-a2e4-1f007222445c)




