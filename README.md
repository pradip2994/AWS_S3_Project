# Created a Website Hosting Setup Using AWS S3, CloudFront, AWS Certificate Manager and Route 53.

![s3](https://github.com/pradip2994/S3_Website_Project/assets/124191442/94a7cac7-41b7-4acf-8d6c-9e6cce832198)


# Below are the steps to host a website. 

## WEBSITE PREVIEW 
![Screenshot 2023-10-11 234003](https://github.com/pradip2994/S3_Website_Project/assets/124191442/d9a0c988-4d57-4c7b-8eb1-e54eda5ede31)


## Route53
### Purchase a domain.
### Create a hosted zone.
### Update the name servers if you have purchased the domain from another registrar.

![Screenshot 2023-10-11 224019](https://github.com/pradip2994/S3_Website_Project/assets/124191442/6eae8b3a-4195-4532-8ec3-7f31625a89bd)



## Aws certificate manager

### Create custom SSL certificate.
### Navigate to aws certificate manager.
### Select region N.Virginia.

![Screenshot 2023-10-11 231202](https://github.com/pradip2994/S3_Website_Project/assets/124191442/6333f9e9-b88f-4b7b-a5ac-a34bcade1016)


### Click on request a certificate.
### Select request for public certificate then click on next.

![Screenshot 2023-10-11 231210](https://github.com/pradip2994/S3_Website_Project/assets/124191442/765e645c-e287-4848-bd47-52474837b6aa)


### Enter the domains then click on request.

![Screenshot 2023-10-11 231238](https://github.com/pradip2994/S3_Website_Project/assets/124191442/52cc8ad9-0153-4ccb-b30c-aa883c64c42a)


### Now certificate has been created click on Certificate ID.

![Screenshot 2023-10-11 231256](https://github.com/pradip2994/S3_Website_Project/assets/124191442/5e736438-ec0a-4900-b5b7-c0d992721798)

![Screenshot 2023-10-11 231306](https://github.com/pradip2994/S3_Website_Project/assets/124191442/21bf1285-9dfe-4ba9-bb9b-a69eac2f0662)


### Then click on create records in route 53.

![Screenshot 2023-10-11 231312](https://github.com/pradip2994/S3_Website_Project/assets/124191442/38c41cf3-fe8f-4d88-823a-e786cd4b18e5)


### Records has been created.

![Screenshot 2023-10-11 231321](https://github.com/pradip2994/S3_Website_Project/assets/124191442/3f57ad83-5388-440f-b78c-ea63c0c18fb0)


### Now navigate to route 53 and check in hosted zones, Click on domain which you have created, you can see in records CNAME is created. 

![Screenshot 2023-10-11 231355](https://github.com/pradip2994/S3_Website_Project/assets/124191442/cd02fa98-e46e-4418-a639-c7110df6d69a)

![Screenshot 2023-10-11 231406](https://github.com/pradip2994/S3_Website_Project/assets/124191442/fed99928-bf19-43af-8a96-1cccb3c93bab)


## AWS S3 (Simple storage service)

### Create bucket with Domain.  

### Select region N.Virginia.

![Screenshot 2023-10-11 231514](https://github.com/pradip2994/S3_Website_Project/assets/124191442/19b09965-eb91-4b2f-aafe-cf97c917271f)


### Untick the Block public access And tick the box I acknowledged.

![Screenshot 2023-10-11 231529](https://github.com/pradip2994/S3_Website_Project/assets/124191442/39a826f9-110b-48db-9e8c-bc09ac255f0c)


### Then click on create bucket.

![Screenshot 2023-10-11 231543](https://github.com/pradip2994/S3_Website_Project/assets/124191442/b6f2cb15-df07-42ff-bb85-26f5033d5e07)


### Now enter into bucket And click on properties

![Screenshot 2023-10-11 231558](https://github.com/pradip2994/S3_Website_Project/assets/124191442/06d4be77-f371-4f1d-9dac-2fba184a0881)

![Screenshot 2023-10-11 231633](https://github.com/pradip2994/S3_Website_Project/assets/124191442/5b0c9c59-3fe7-4a63-91ac-64dd233693fd)


### In static website hosting session click on edit select enable.

![Screenshot 2023-10-11 231644](https://github.com/pradip2994/S3_Website_Project/assets/124191442/76e95a8a-c9de-4968-aef1-992764583513)


### Enter the index document that is index.html then click on save changes.

![Screenshot 2023-10-11 231722](https://github.com/pradip2994/S3_Website_Project/assets/124191442/15016d2e-1f06-4740-b4a1-4a266d2c1eaf)


### Now click on permissions 

![Screenshot 2023-10-11 231801](https://github.com/pradip2994/S3_Website_Project/assets/124191442/78fd3b96-d73a-41f1-a5d9-3c8bd1538093)


### Create bucket policy with action Get Object 

![Screenshot 2023-10-11 231951](https://github.com/pradip2994/S3_Website_Project/assets/124191442/a65e7719-58b9-4213-8ca5-29e8737620a6)


### Now upload the content in bucket.

![Screenshot 2023-10-11 232221](https://github.com/pradip2994/S3_Website_Project/assets/124191442/c49ef058-c505-4336-bc39-691ac5dd954b)


### Now create another bucket for Sub Domain.

![Screenshot 2023-10-11 232323](https://github.com/pradip2994/S3_Website_Project/assets/124191442/2f3a10dd-fd16-4ae4-bcb2-30fbaaa4716d)


### Enter bucket name.
### Select region N.Virginia.
### Then you click on create bucket.

![Screenshot 2023-10-11 232341](https://github.com/pradip2994/S3_Website_Project/assets/124191442/d2fc536b-9cfa-4b27-8658-211e25debcce)

### Sub Domain bucket has been created.

![Screenshot 2023-10-11 232356](https://github.com/pradip2994/S3_Website_Project/assets/124191442/852ab68f-5d1b-4f19-bf36-d0c6665d9bd0)


### Enter inside the bucket go to properties

![Screenshot 2023-10-11 232417](https://github.com/pradip2994/S3_Website_Project/assets/124191442/0f7a38a0-8d6b-4ae4-842d-119fd9a01875)


### In static website hosting session click on edit select enable, And then click on redirect request for an object.
### enter the host name you want to redirect select protocol https then click on save changes. 

![Screenshot 2023-10-11 232523](https://github.com/pradip2994/S3_Website_Project/assets/124191442/8fc64ffb-6b15-4eab-8404-12f5cbfe765e)


## CloudFront

### Navigate to cloud front create cloud front distribution.
### Click on create a CloudFront distribution. and then click On create distribution. 

![Screenshot 2023-10-11 232634](https://github.com/pradip2994/S3_Website_Project/assets/124191442/fce76df1-9b2c-4bb5-ab79-17a576b97ad0)


### Now copy and paste the static web hosting endpoint of Domain bucket to origin Domain.

![Screenshot 2023-10-11 232736](https://github.com/pradip2994/S3_Website_Project/assets/124191442/5cc14fec-f566-4891-8406-1418890b8f6f)

![Screenshot 2023-10-11 232825](https://github.com/pradip2994/S3_Website_Project/assets/124191442/1f1c936f-db1e-49e1-8ef1-0e6145ec8f78)


### In viewer section click on redirect HTTP to HTTPS.

![Screenshot 2023-10-11 232847](https://github.com/pradip2994/S3_Website_Project/assets/124191442/3019aa73-ced8-49da-a390-465e4dc93828)


### Click on Do not enable security protections.
### In settings section add CNAME choose SSL certificate and then click on create distribution.

![Screenshot 2023-10-11 232935](https://github.com/pradip2994/S3_Website_Project/assets/124191442/0557b09e-9b17-4c44-91af-7ae9eb23f4ef)

![Screenshot 2023-10-11 232948](https://github.com/pradip2994/S3_Website_Project/assets/124191442/54775e5b-0784-4f5d-b22c-d644bc22f8a7)


### Now we can see that for Domain CloudFront has been created.

![Screenshot 2023-10-11 233002](https://github.com/pradip2994/S3_Website_Project/assets/124191442/49adeae7-bc6e-4ab7-8b7f-89404d030c09)


### Copy and paste the static web hosting endpoint of SubDomain bucket to Origin Domain.

![Screenshot 2023-10-11 233037](https://github.com/pradip2994/S3_Website_Project/assets/124191442/d2473aa5-a586-4d09-9d4b-7c6ff7be242c)

![Screenshot 2023-10-11 233117](https://github.com/pradip2994/S3_Website_Project/assets/124191442/d81d4803-d686-474e-bfcd-f8707bd83252)


### In Viewer section click on redirect HTTP to HTTPS.

![Screenshot 2023-10-11 233142](https://github.com/pradip2994/S3_Website_Project/assets/124191442/1e43ae93-2d61-49a6-8620-1525638c92a6)


### Click on Do not enable security protections.
### In settings section add CNAME of SubDomain choose SSL certificate and then click on create distribution.

![Screenshot 2023-10-11 233234](https://github.com/pradip2994/S3_Website_Project/assets/124191442/f9c8660b-18d6-4c70-8961-f6cd6b53a576)

![Screenshot 2023-10-11 233246](https://github.com/pradip2994/S3_Website_Project/assets/124191442/2b18eb21-3caf-404b-af80-3b8203b7fdc7)


### Now we can see that for SubDomain CloudFront has been created.
![Screenshot 2023-10-11 233301](https://github.com/pradip2994/S3_Website_Project/assets/124191442/f4f6762a-bc27-4946-a827-631414de8c0e)


### Now again navigate to route 53 go to hosted zone click on domain and create Record.

![Screenshot 2023-10-11 233403](https://github.com/pradip2994/S3_Website_Project/assets/124191442/652e78f9-70ed-49b0-b59b-37d605c03029)


### Create a Record, record-1 and record-2 for domain and for sub domain.
### Click on alias choose where to route traffic to.
### Click on cloudfront distribution alias 
### Select the region and select simple routing policy then click on create records.

![Screenshot 2023-10-11 233610](https://github.com/pradip2994/S3_Website_Project/assets/124191442/4f783bdc-6b5a-4935-bcf3-c3f83dc47eb2)


### In the below image we can see that record has been created in hosted zone.

![Screenshot 2023-10-11 233834](https://github.com/pradip2994/S3_Website_Project/assets/124191442/15dff06f-a7ea-49d0-82b4-1afc01e14433)


So, finally everything is done now we can access website using domain and sub domain.

![Screenshot 2023-10-11 234003](https://github.com/pradip2994/S3_Website_Project/assets/124191442/59267e49-5e02-47cd-a547-0b6ef080540f)


