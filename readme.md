# Static Website Hosting using AWS S3, CloudFront, and GoDaddy

## 📌 Overview
This project demonstrates how to **host a static website** using **Amazon S3**, deliver it globally via **Amazon CloudFront**, and optionally connect it to a **custom domain purchased from GoDaddy**.  
The setup ensures high availability, low latency, and secure content delivery.

---

## 🧠 Concept
The core idea of this project is to create a **fully serverless static site hosting architecture** using AWS services.  
The workflow involves:

- Uploading static site files (HTML, CSS, JS) to an **S3 bucket**
- Configuring the bucket for static hosting
- Creating a **CloudFront distribution** to cache and deliver the content globally
- Mapping a **custom domain** (like from GoDaddy) to the CloudFront distribution using DNS records

---

## 🏗️ Architecture

Below is the high‑level architecture flow:

```
User → DNS (GoDaddy) → CloudFront CDN → S3 Bucket → Static Website
```

### Architecture Images
![architecture](images/architecture.png)

#### CloudFront Distribution  
![CloudFront](images/CF1.png)
![CloudFront](images/CF2.png)

#### S3 Bucket Objects  
![S3](images/S31.png)
![S3](images/S32.png)
![S3](images/S33.png)
![S3](images/S34.png)


## 📄 index.html File

Below is the complete code used for hosting the static website:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Static Website</title>

    <!-- Google Font -->
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
        // Auto-insert deployment date & time
        document.getElementById("time").textContent = new Date().toLocaleString();
    </script>

</body>
</html>




#### Final Hosted Website  
![Hosted Site](images/result.png)

---

## 🚀 Features
- Fully serverless hosting solution  
- Global edge caching improves speed  
- Extremely low cost (eligible for free tier)  
- Easy deployments — just upload new files to S3  
- Secure delivery via HTTPS (when using ACM certificates)  
- Optional custom domain support

---

## 📁 Tech Stack
- **Amazon S3** — static site hosting  
- **Amazon CloudFront** — CDN caching + HTTPS delivery  
- **GoDaddy** — domain management  
- **VSCode + GitHub** — source control & deployment  

---

## 🔧 Steps Involved
1. Create an **S3 bucket** and upload website files  
2. Enable static hosting and set correct permissions  
3. Create a **CloudFront distribution** pointing to S3  
4. Update DNS on **GoDaddy** to map domain → CloudFront  
5. Test website using CloudFront URL & custom domain  
6. Push project to **GitHub** with this README  

---

## 📝 Summary
This project is a perfect introduction to serverless hosting using AWS. It provides a fast, scalable, and cost-efficient solution for any static website.  
By integrating S3, CloudFront, and GoDaddy, you gain global content delivery with custom branding.

---

### ✨ Author  
**Vishal Suresh Chavan**



