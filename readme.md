# Static Website Hosting using AWS S3, CloudFront, and GoDaddy

## 📌 Overview

This project demonstrates how to **host a static website** using
**Amazon S3**, deliver it globally using **Amazon CloudFront**, and
optionally map it to a **custom domain from GoDaddy**.\
This architecture ensures **low latency, high availability, global
reach, and secure HTTPS delivery**.

## 🧠 Concept

The idea behind this project is to create a **fully serverless,
scalable, and cost-efficient static hosting setup**.

## 🏗️ Architecture

    User → DNS (GoDaddy) → CloudFront CDN → S3 Bucket → Static Website

### Architecture Image

![architecture](images/architecture.png)

## 🌐 CloudFront Distribution

![CloudFront 1](images/CF1.png)\
![CloudFront 2](images/CF2.png)

## 📦 S3 Bucket Objects

![S3 1](images/S31.png)\
![S3 2](images/S32.png)\
![S3 3](images/S33.png)\
![S3 4](images/S34.png)

## 🌍 Final Hosted Website

![Hosted Site](images/result.png)

# 📄 index.html File

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Static Website</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

    <style>
        body {
            margin: 0;
            font-family: "Poppins", sans-serif;
            background: linear-gradient(135deg, #4f46e5, #7c3aed);
            color: white;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }
        .container {
            background: rgba(255, 255, 255, 0.12);
            padding: 40px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            max-width: 700px;
            animation: fadeIn 1.5s ease-in-out;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
        }
        h1 {
            margin: 0;
            font-size: 2.8rem;
            font-weight: 600;
        }
        p {
            font-size: 1.2rem;
            margin-top: 15px;
            opacity: 0.9;
        }
        .tag {
            margin-top: 20px;
            display: inline-block;
            padding: 10px 20px;
            background: #ffffff22;
            border-radius: 50px;
            font-size: 1rem;
        }
        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px);}
            100% { opacity: 1; transform: translateY(0);}
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🚀 Welcome to My Static Website</h1>
        <p>This website is hosted on <strong>Amazon S3</strong> and delivered globally with <strong>CloudFront CDN</strong>.</p>
        <p>Domain is configured using <strong>GoDaddy</strong>.</p>
        <div class="tag">
            Deployment Time: <span id="time"></span>
        </div>
    </div>
    <script>
        document.getElementById("time").textContent = new Date().toLocaleString();
    </script>
</body>
</html>
```

## 🚀 Features

-   Serverless hosting\
-   CDN caching\
-   HTTPS with ACM\
-   Custom domains

## 📁 Tech Stack

-   Amazon S3\
-   Amazon CloudFront\
-   GoDaddy\
-   VSCode + GitHub

## 🔧 Steps Involved

1.  Create S3 bucket\
2.  Enable hosting\
3.  Configure policy\
4.  Create CloudFront\
5.  Configure DNS\
6.  Deploy

## 📝 Summary

This project showcases scalable static website hosting using AWS
services.

### ✨ Author

**Vishal Suresh Chavan**
