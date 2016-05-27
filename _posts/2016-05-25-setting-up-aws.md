---
layout: post
title:  "Setting up AWS "
date:   2016-05-25 13:19:21 -0500
categories: AWS S3
---
Setting up AWS for static website hosting.

---
layout: post
title:  Hosting a static website on AWS
---
I've decided that I want to host my personal STATIC websites on AWS.

I'm going to use Jekyll(www.jekyllrb.com) as my static site generator.

I followed this step by step guide http://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html

I bought my domain through http://www.namecheap.com


Creating buckets http://docs.aws.amazon.com/AmazonS3/latest/UG/CreatingaBucket.html

Uploading object to bucket http://docs.aws.amazon.com/AmazonS3/latest/UG/UploadingObjectsintoAmazonS3.html

Edit bucket permissions http://docs.aws.amazon.com/AmazonS3/latest/UG/EditingBucketPermissions.html
Add bucket policy

`{
  "Version":"2012-10-17",
  "Statement":[{
	"Sid":"AddPerm",
        "Effect":"Allow",
	  "Principal": "*",
      "Action":["s3:GetObject"],
      "Resource":["arn:aws:s3:::learnstem.tech/*"
      ]
    }
  ]
}`

learnstem.tech Endpoint: learnstem.tech.s3-website-us-west-2.amazonaws.com

Configure bucket for website Hosting http://docs.aws.amazon.com/AmazonS3/latest/UG/ConfiguringBucketWebsite.html


add bower and grunt to Jekyll http://www.aymerick.com/2014/07/22/jekyll-github-pages-bower-bootstrap.html
