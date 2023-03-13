---
title: "ILLA Cloud New V1.40 Amazon / Generic S3"
seoTitle: "ILLA Cloud New V1.40 Amazon / Generic S3"
seoDescription: "n ILLA's 1.40 Version, we started to support S3. The ILLA S3 Resource can connect to Amazon S3, Upcloud, Digital Ocean Spaces, Wasabi and more"
datePublished: Fri Dec 02 2022 07:50:01 GMT+0000 (Coordinated Universal Time)
cuid: cldvdfyz4000b09mi8ab6gbc3
slug: illa-cloud-new-v140-amazon-generic-s3
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1675842317030/d2d2ebde-e6ea-494d-b140-b069a71693c0.png
tags: databases, developer, amazon-s3, low-code, illa

---

Amazon S3 (Amazon Simple Storage Service) is a service offered by Amazon Web Services (AWS) that provides object storage through a web service interface. Amazon S3 manages data with an object storage architecture that aims to provide scalability, high availability, and low latency with high durability.

![A brief intro to Amazon S3](https://cdn.hashnode.com/res/hashnode/image/upload/v1675842390661/87d323c4-87ae-49a3-a585-80e3d02306f4.png align="left")

<center><figcaption>A brief intro to Amazon S3</figcaption></center>

There are many advantages of Amazon S3:

* Provides a unified interface REST/SOAP to uniformly access any data
    
* Data stored in S3 is the object name (key), and the data (value)
    
* Large file capability, up to 5TB for a single file
    
* High speed. Up to 3500 PUT/COPY/POST/DELETE or 5500 GET/HEAD per second per bucket
    
* Capable of version and authority control
    
* Capable of data lifecycle management
    

In ILLA’s 1.40 Version, we started to support S3. The ILLA S3 Resource can connect to Amazon S3, Upcloud, Digital Ocean Spaces, Wasabi, DreamObjects, MinIO, and any other S3 provider. Below, you will see examples of connecting to your S3 provider and issuing List, Create, Read, and Delete actions.

## [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#configure-s3-resource)**Configure S3 Resource**

![Configure S3 Resource](https://cdn.hashnode.com/res/hashnode/image/upload/v1675842394974/608de041-4ee3-496c-b479-12a53ab9e37f.png align="left")

The S3 Resource requires the following information to establish a connection:

1. Amazon S3 Bucket Region
    
2. Amazon Access Key ID
    
3. Amazon Secret Key
    

For Amazon S3, you can find your Access Key and Secret Key using the following guide: Accessing AWS using your AWS credentials

And the following optional information:

1. Bucket name( used to specify the bucket )
    
2. Custom S3 endpoint ( used to connect to other non-S3 services, like Digital Ocean Spaces, Wasabi, and so on )
    

## [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#configure-actions)**Configure actions**

### [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#list-all-objects-in-a-bucket)**List all objects in a bucket**

This action lists the files in the bucket. It will return an array of objects, each including at least one `objectKey` property.

![ObjectKey](https://cdn.hashnode.com/res/hashnode/image/upload/v1675842419386/879fd47a-b476-4abf-b3c2-b178a9fadf6e.png align="left")

This action contains the following optional information:

![optional information](https://cdn.hashnode.com/res/hashnode/image/upload/v1675842466426/468e121f-87c3-4334-be43-5bc1dea644c3.png align="left")

1. Bucket name: This can be left out if you have filled in the bucket name when configuring the S3 resource. If not, this is required.
    
2. Prefix to filter results: To narrow your query to return only files that begin with your specified prefix.
    
3. Delimiter: Used to group object keys.
    
4. Generate Signed URL: If YES, the action will return a signed URL.
    
5. Expiry Duration of Signed URL(Minutes): To set the expiry duration of the signed URL.
    
6. Max keys: To set the maximum number of keys returned in the response.
    

### [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#read-an-object)**Read an object**

This action lists an array of objects, including `objectData` property. It contains the following optional information:

1. Bucket name
    
2. Object key
    

### [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#download-an-object)**Download an object**

This action will automatically download the file which matches the object key. It contains the following optional information:

1. Bucket name
    
2. Object key
    

### [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#delete-an-object)**Delete an object**

This action will delete the file which matches the object key. It contains the following optional information:

1. Bucket name
    
2. Object key
    

### [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#delete-multiple-objects)**Delete multiple objects**

This action will delete multiple files which match the object keys. It contains the following optional information:

1. Bucket name
    
2. Object key list: a list of object keys to delete.
    

### [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#upload-data)**Upload data**

This action allows users to upload a file to an S3 bucket. It contains the following information:

1. Bucket name
    
2. Content-type: text/plain, image/bmp, application/pdf, and so on.
    
3. Upload object name: to override the file name.
    
4. Upload data: base64 encoded data.
    

### [**​**](https://www.illacloud.com/blog/illa-cloud-new-amazon-s3#upload-multiple-data)**Upload multiple data**

This action allows users to upload multiple files to the S3 bucket. It contains the following information:

1. Bucket name
    
2. Content-type
    
3. Upload object name list: a list of file names.
    
4. Upload data list: a list of base64 encoded data.
    

![Upload multiple data](https://cdn.hashnode.com/res/hashnode/image/upload/v1675842499487/45d2b1af-33a8-4271-ac50-a1972d400774.gif align="left")

> #### ***You can check ILLA’s website here at:*** [***https://illacloud.com***](https://illacloud.com)
> 
> #### ***GitHub page:*** [***https://github.com/illacloud/illa-builder***](https://github.com/illacloud/illa-builder)
> 
> #### ***Join Discord community:*** [***https://discord.com/invite/illacloud***](https://discord.com/invite/illacloud)