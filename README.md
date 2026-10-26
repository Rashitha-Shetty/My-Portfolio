# Rashitha Shetty — Portfolio Website & Multi-Architecture AWS Deployment

A responsive personal portfolio website deployed across multiple Amazon Web Services (AWS) architectures—from serverless storage (S3) to a full Linux virtual server (EC2 with Apache).

---

## 🌐 Live Website Links

- **S3 Static Deployment (Serverless):** [View S3 Portfolio Site](http://rashitha-portfolio-2026.s3-website-ap-southeast-2.amazonaws.com)
- **EC2 Linux Server Deployment (IaaS):** `http://3.104.1.200/My-Portfolio/`

---

## 🛠️ Technologies & Tools Used

- **Frontend:** HTML5, CSS3
- **Cloud Infrastructure:** AWS S3, AWS EC2 (Ubuntu 24.04 LTS), AWS VPC, Security Groups
- **Web Server:** Apache2 HTTP Server
- **Version Control & Remote Access:** Git, GitHub, SSH CLI, Linux Terminal

---

## 🚀 AWS Architecture & Implementation Details

### Architecture 1: Amazon S3 Static Website Hosting (Serverless)
* **Storage:** Created an Amazon S3 general-purpose bucket.
* **Access Control:** Configured public bucket policies and disabled Block Public Access settings for web visibility.
* **Hosting:** Enabled static website hosting with `index.html` as the root document.
* **Testing:** Verified site responsiveness across mobile and desktop browsers.

### Architecture 2: AWS EC2 Linux Web Server (Virtual Server / IaaS)
* **Instance Provisioning:** Launched an Ubuntu 24.04 LTS `t2.micro` EC2 instance in AWS.
* **Network Security:** Configured custom Security Group inbound rules allowing:
  - **SSH (Port 22):** Secure remote administrative terminal access via `.pem` key.
  - **HTTP (Port 80):** Public web access (`0.0.0.0/0`).
* **Web Server Configuration:** 
  - Installed and enabled Apache2 HTTP web server daemons using Linux `systemctl` and `apt`.
  - Cloned production portfolio files directly into Apache web directories using Git.
* **Operations & Monitoring:** Inspected live access and error logs in `/var/log/apache2/`.

---

## 💡 What I Learned

- S3 object storage vs. EC2 virtual computing.
- Bucket policies, Security Groups, and network port management (Port 22 & Port 80).
- Remote server management over SSH.
- Linux package installation, system services (`systemctl`), and system logs.

---

## 📌 Future Improvements

- Automate AWS infrastructure using **Terraform (Infrastructure as Code)**.
- Secure HTTP web traffic with HTTPS/TLS certificates using Amazon CloudFront / Let's Encrypt.
- Containerize application using **Docker** and build an automated **GitHub Actions CI/CD Pipeline**.
