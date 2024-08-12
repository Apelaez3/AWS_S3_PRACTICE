# AWS_S3_PRACTICE
respositorio creado para desarrollar la creacion de un sitio web estatio que sea despleagado con github actions a un buckect de S3 

## Deploy static website to s3 using github actions 

1.	The first thing that I have made was create an user in iam. 
<img width="442" alt="image" src="https://github.com/user-attachments/assets/ba5ea440-9195-4951-bc6e-94a4cf8e0bd7">

 
2.	To be able to create the user, I used the CLI,  here are the commands used: 
a.	aws iam create-user --user-name my-new-user 
b.	aws iam create-access-key --user-name my-new-user

3.	Once I had the access  key id and the secret access key ,  click on the user created and went to permission. 

 <img width="442" alt="image" src="https://github.com/user-attachments/assets/d19d8d7a-bc97-4ce6-a062-6704400c73d4">


4.	In this step, I selected the "Add permissions" option and chose "AmazonS3FullAccess."

5.	Then, I went to the repository, clicked on "Settings" > "Secrets" > "Actions."

6.	 In this section, I created a new repository secret and added the access key and the secret key.
 <img width="442" alt="image" src="https://github.com/user-attachments/assets/1d2397f7-c98b-4361-96c5-6db2b493f46d">


7.	Next, within the repository, I navigated to "Actions" and set up the first workflow. I used the following code:
8.<img width="442" alt="image" src="https://github.com/user-attachments/assets/f8a8babe-8db0-4e4d-b413-bdf7b49fc691">
	 
9.	Once I committed the changes, the workflow started running and displayed a green checkmark.
10.	Afterward, I went to the AWS S3 bucket and verified that the files were uploaded successfully
<img width="442" alt="image" src="https://github.com/user-attachments/assets/4491106b-91d5-4731-9591-ece494f0b8a8">


