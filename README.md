# ☁️ AWS S3 Static Website Hosting

This project demonstrates how to host a **static website using Amazon S3** and make it publicly accessible via a website URL.

---

## 🎯 Objective

To create and deploy a simple static website using **Amazon S3** with public access enabled.

---

## 🚀 Features

* 🌐 Static website hosting using AWS S3
* 📄 Simple HTML webpage
* 🔓 Public access enabled via bucket policy
* 🔗 Accessible through S3 website endpoint

---

## 🛠️ Technologies Used

* HTML5
* Amazon Web Services (AWS S3)

---

## 📁 Project Structure

```bash
aws-s3-static-website/
│── index.html
│── README.md
```

---

## ⚙️ Deployment Steps

### 1️⃣ Create S3 Bucket

* Go to AWS Console → S3
* Click **Create Bucket**
* Enter a **unique bucket name**
* Select region and create bucket

---

### 2️⃣ Upload Website Files

* Open your bucket
* Click **Upload**
* Add `index.html`
* Click **Upload**

---

### 3️⃣ Enable Static Website Hosting

* Go to **Properties** tab
* Scroll to **Static Website Hosting**
* Click **Edit** → Enable
* Set:

  * Index document: `index.html`

---

### 4️⃣ Make Bucket Public

Add the following **Bucket Policy**:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicRead",
      "Effect": "Allow",
      "Principal": "*",
      "Action": ["s3:GetObject"],
      "Resource": ["arn:aws:s3:::your-bucket-name/*"]
    }
  ]
}
```

---

## 🌍 Live Website

👉 **S3 Website URL:**

```

https://bisht-assignment-ciphers.s3.eu-north-1.amazonaws.com/index.html

```

---

## 📬 Conclusion

This project helped in understanding:

* AWS S3 basics
* Static website hosting
* Bucket policies and public access

---

## 📄 License

This project is for educational purposes.
