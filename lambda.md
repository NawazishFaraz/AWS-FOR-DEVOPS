# **What is AWS Lambda?**

AWS Lambda is a **serverless compute service** provided by Amazon Web Services (AWS). It enables developers to run code without provisioning or managing servers. With Lambda, you can focus solely on writing and deploying code, while AWS handles the infrastructure, scaling, and maintenance.

---

## **Key Features of AWS Lambda**
- **Serverless Architecture**: No need to manage servers or infrastructure; AWS handles everything.
- **Event-Driven**: Executes code in response to events such as HTTP requests, file uploads to S3, database updates, or custom triggers.
- **Pay-As-You-Go**: Charges only for the compute time consumed, with no charges for idle time.
- **Scalability**: Automatically scales based on the number of requests, accommodating variable workloads seamlessly.
- **Multi-Language Support**: Supports various programming languages like Python, JavaScript (Node.js), Java, Go, Ruby, and more.

---

## **Example of an AWS Lambda Workflow**

1. A user uploads an image to an **S3 bucket**.
2. The **S3 event** triggers a **Lambda function**.
3. The **Lambda function** processes the image (e.g., resizes it).
4. The **processed image** is stored in another **S3 bucket**.



## **How AWS Lambda Works**
1. **Write Code**: Develop a function in one of the supported programming languages.
2. **Upload Function**: Upload the code as a ZIP file or container image to AWS Lambda.
3. **Configure Trigger**: Set up an event source (e.g., API Gateway, S3 bucket, DynamoDB table) to invoke the function.
4. **Execute**: AWS Lambda executes the function in response to the trigger.
