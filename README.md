# DevOps-09-AWS-js-app

This demo project shows how to push a docker image to **AWS ECR**.

---

## 1. Build the Docker Image

Build the Docker image and tag it as `my-app:1.0`:

```bash
docker build -t my-app:1.0 .
```

---

## 2. Create a Private ECR Repository

In the AWS Console:

* Go to **Amazon ECR** → **Create a repository**.
* Set the repository visibility to **Private**.
* Set the repository name to `my-app`.
* Click **Create repository**.

---

## 3. Install and Configure the AWS CLI

### 3.1 Install AWS CLI

Install the AWS CLI if it is not already installed:

```bash
curl -fsSL https://awscli.amazonaws.com/v2/install.sh | sudo bash -s -- --system
```

### 3.2 Configure AWS Credentials

Configure your AWS credentials:

```bash
aws login
```

---

## 4 Push the Image to Amazon ECR
Open the `my-app` repository in Amazon ECR.

Click on **View push commands**.

AWS provides the commands required to:

1. Authenticate Docker with Amazon ECR.
2. Tag the local Docker image with the ECR repository URI.
3. Push the image to the repository.

Just follow the commands provided by AWS.

---

## 5. Verify the Image

To verify that the image was successfully pushed:

1. Open **Amazon ECR** in the AWS Console.
2. Open the `my-app` repository.
3. Check that the image with the tag `1.0` is listed.

---

## Acknowledgements

This demo project was created as part of the DevOps Bootcamp by **TechWorld with Nana**.

Many thanks to Nana for creating such a comprehensive and practical learning experience.
