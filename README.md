# Creating a Website Hosting Setup Using AWS S3, CloudFront, AWS Certificate Manager and Route 53.

![Screenshot 2023-09-18 060832](https://github.com/pradip2994/S3_Website_Project/assets/124191442/77fcb13f-3733-432b-92ee-3b0ab66cbe0c)

# Below are the steps to host a website. 

## WEBSITE PREVIEW 
![Screenshot 2023-09-18 065743](https://github.com/pradip2994/S3_Website_Project/assets/124191442/ba5a63af-cef9-4b4a-858e-2be9787a3cd4)

## Route53
### Purchase a domain.
### Create a hosted zone.
### Update the name servers if you have purchased the domain from another registrar.

![Screenshot 2023-09-18 061338](https://github.com/pradip2994/S3_Website_Project/assets/124191442/2b3e4a84-227e-41c8-b9ed-8ee7c9b58e4a)


## Aws certificate manager

### Create custom SSL certificate.
### Navigate to aws certificate manager.

![Screenshot 2023-09-18 061428](https://github.com/pradip2994/S3_Website_Project/assets/124191442/21350fda-846d-4cc1-87df-7541cbea8403)

### Click on request a certificate.
### Select request for public certificate then click on next.

![Screenshot 2023-09-18 061448](https://github.com/pradip2994/S3_Website_Project/assets/124191442/32bf546a-7e7b-4aa0-b660-80d377947cc2)

### Enter the domains then click on request.

![Screenshot 2023-09-18 061651](https://github.com/pradip2994/S3_Website_Project/assets/124191442/cef181de-cb55-40a3-a1ee-ca8fb04e55a8)

### Now certificate has been created click on Certificate ID.

![Screenshot 2023-09-18 061714](https://github.com/pradip2994/S3_Website_Project/assets/124191442/150f836c-b81f-4de9-944f-4f77f43ca792)
![Screenshot 2023-09-18 061745](https://github.com/pradip2994/S3_Website_Project/assets/124191442/4ada39b0-b749-4a9a-a93c-c64b5b1f5f50)

### Then click on create records in route 53.

![Screenshot 2023-09-18 061814](https://github.com/pradip2994/S3_Website_Project/assets/124191442/f6a6f1a1-e031-4f01-a722-908e504b3f13)

### Records has been created.

![Screenshot 2023-09-18 061907](https://github.com/pradip2994/S3_Website_Project/assets/124191442/cc79d0cc-26bf-4aaf-8cba-065a9c5221ce)

### Now navigate to route 53 and check in hosted zones, Click on domain which you have created, you can see in records CNAME is created. 

![Screenshot 2023-09-18 061922](https://github.com/pradip2994/S3_Website_Project/assets/124191442/52127d5b-2605-4c2a-820d-153387a2fb2a)
![Screenshot 2023-09-18 062019](https://github.com/pradip2994/S3_Website_Project/assets/124191442/6b415ce8-cb75-4c34-84c1-688dc8dd6bd3)

## AWS S3 (Simple storage service)

### Create bucket with Domain.  

### Select region N.Virginia.

![Screenshot 2023-09-18 062220](https://github.com/pradip2994/S3_Website_Project/assets/124191442/35dd5a2d-c5aa-4379-809f-43a276319dda)

### Untick the Block public access And tick the box I acknowledged.

![Screenshot 2023-09-18 062244](https://github.com/pradip2994/S3_Website_Project/assets/124191442/1651187a-62e6-44f3-b75d-d1a19c42e2ad)

### Then click on create bucket.

![Screenshot 2023-09-18 062305](https://github.com/pradip2994/S3_Website_Project/assets/124191442/07ce05d9-2bc3-468d-85cb-da06ab50336a)

### Now enter into bucket And click on properties

![Screenshot 2023-09-18 062317](https://github.com/pradip2994/S3_Website_Project/assets/124191442/67a40243-13dd-4183-81f7-ab228494f680)
![Screenshot 2023-09-18 062416](https://github.com/pradip2994/S3_Website_Project/assets/124191442/cb90ca7e-8526-4909-b2ab-88f28f447343)

### In static website hosting session click on edit select enable.

![Screenshot 2023-09-18 062429](https://github.com/pradip2994/S3_Website_Project/assets/124191442/076896f5-6b7a-4f9e-8431-584cbd9175c5)

### Enter the index document that is index.html then click on save changes.

![Screenshot 2023-09-18 062519](https://github.com/pradip2994/S3_Website_Project/assets/124191442/84988b59-4a41-425a-aea7-575f1ea82aa7)

### Now click on permissions 

![Screenshot 2023-09-18 062602](https://github.com/pradip2994/S3_Website_Project/assets/124191442/b6416b9b-4554-402a-ab61-24c694c441e9)

### Create bucket policy with action Get Object 

![Screenshot 2023-09-18 062852](https://github.com/pradip2994/S3_Website_Project/assets/124191442/4230d2d2-9c5a-411b-8523-107049d8c8a0)

### Now upload the content in bucket.

![Screenshot 2023-09-18 063028](https://github.com/pradip2994/S3_Website_Project/assets/124191442/2f622ab2-e072-4c8e-946f-5170864ee77d)

### Now create another bucket for Sub Domain.

![Screenshot 2023-09-18 063139](https://github.com/pradip2994/S3_Website_Project/assets/124191442/0994d488-067a-460e-b69c-29e5c58fcac2)

### Enter bucket name.
### Select region N.Virginia.
### Then you click on create bucket.

![Screenshot 2023-09-18 063201](https://github.com/pradip2994/S3_Website_Project/assets/124191442/1bad6809-3348-45dd-abeb-2814665021bb)
### Sub Domain bucket has been created.

![Screenshot 2023-09-18 063221](https://github.com/pradip2994/S3_Website_Project/assets/124191442/6bc74666-8801-43aa-a18c-a6c2824c63e5)

### Enter inside the bucket go to properties

![Screenshot 2023-09-18 063251](https://github.com/pradip2994/S3_Website_Project/assets/124191442/c0d5f197-758e-49fa-9bb4-46c2cfe3846b)

### In static website hosting session click on edit select enable, And then click on redirect request for an object.
### enter the host name you want to redirect select protocol https then click on save changes. 

![Screenshot 2023-09-18 063333](https://github.com/pradip2994/S3_Website_Project/assets/124191442/c0378fda-59c0-463c-a496-692d5a0da549)

## CloudFront

### Navigate to cloud front create cloud front distribution.
### Click on create a CloudFront distribution. and then click On create distribution. 

![Screenshot 2023-09-18 063632](https://github.com/pradip2994/S3_Website_Project/assets/124191442/3e9fc3f6-590c-4aac-9a41-b6d5457c597c)

### Now copy and paste the static web hosting endpoint of Domain bucket to origin Domain.

![Screenshot 2023-09-18 063740](https://github.com/pradip2994/S3_Website_Project/assets/124191442/d53218a8-28f5-46aa-b9bd-ead11cbd6872)
![Screenshot 2023-09-18 063802](https://github.com/pradip2994/S3_Website_Project/assets/124191442/4fa549a0-b097-425b-8412-be8862e1da3b)

### In viewer section click on redirect HTTP to HTTPS.

![Screenshot 2023-09-18 063827](https://github.com/pradip2994/S3_Website_Project/assets/124191442/93064d2b-9475-4f2d-acbf-11124bfb517e)

### Click on Do not enable security protections.
### In settings section add CNAME choose SSL certificate and then click on create distribution.

![Screenshot 2023-09-18 063924](https://github.com/pradip2994/S3_Website_Project/assets/124191442/fc1d8c22-20ba-4f37-995a-7240a56a7f6f)
![Screenshot 2023-09-18 063933](https://github.com/pradip2994/S3_Website_Project/assets/124191442/3be0e110-bc9d-40eb-b9f3-225ef29471fd)

### Now we can see that for Domain CloudFront has been created.

![Screenshot 2023-09-18 064047](https://github.com/pradip2994/S3_Website_Project/assets/124191442/7f0f7c6e-c61e-4d4f-8235-d40c5f53d092)

### Copy and paste the static web hosting endpoint of SubDomain bucket to Origin Domain.

![Screenshot 2023-09-18 064145](https://github.com/pradip2994/S3_Website_Project/assets/124191442/28335f35-3b26-4a13-b482-f60e28cff108)
![Screenshot 2023-09-18 064158](https://github.com/pradip2994/S3_Website_Project/assets/124191442/bc3edb7a-0f0c-4484-85ce-ccf0e1a6646c)

### In Viewer section click on redirect HTTP to HTTPS.

![Screenshot 2023-09-18 064217](https://github.com/pradip2994/S3_Website_Project/assets/124191442/1e13f846-2f54-4911-afce-f86d4bbd1ae8)

### Click on Do not enable security protections.
### In settings section add CNAME of SubDomain choose SSL certificate and then click on create distribution.

![Screenshot 2023-09-18 064307](https://github.com/pradip2994/S3_Website_Project/assets/124191442/f3f69dbe-4b92-4ed9-b43e-ac723461ee13)
![Screenshot 2023-09-18 064319](https://github.com/pradip2994/S3_Website_Project/assets/124191442/286d4fcc-dcf7-4a3e-a5e5-5fd67ba794da)

### Now we can see that for SubDomain CloudFront has been created.
![Screenshot 2023-09-18 064347](https://github.com/pradip2994/S3_Website_Project/assets/124191442/738935a2-2e25-41ea-be71-c0598600b83e)

### Now again navigate to route 53 go to hosted zone click on domain and create Record.

![Screenshot 2023-09-18 064527](https://github.com/pradip2994/S3_Website_Project/assets/124191442/f6e2b614-c091-4c10-bd15-f1e65bf44d93)

### Create a Record, record-1 and record-2 for domain and for sub domain.
### Click on alias choose where to route traffic to.
### Click on cloudfront distribution alias 
### Select the region and select simple routing policy then click on create records.

![Screenshot 2023-09-18 064557](https://github.com/pradip2994/S3_Website_Project/assets/124191442/772040a3-6705-4b69-907a-b956b059080b)
![Screenshot 2023-09-18 064629](https://github.com/pradip2994/S3_Website_Project/assets/124191442/2cdddb60-1f09-4ca0-a486-116765c15c29)

### In the below image we can see that record has been created in hosted zone.

![Screenshot 2023-09-18 064746](https://github.com/pradip2994/S3_Website_Project/assets/124191442/304678fd-fdcc-4527-a476-54e1c2c7708c)

So, finally everything is done now we can access website using domain and sub domain.

![Screenshot 2023-09-18 065743](https://github.com/pradip2994/S3_Website_Project/assets/124191442/c3afcdb8-7826-46b2-905c-26e43e2fbd86)

