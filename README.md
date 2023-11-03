# **Static Website Hosting with Amazon S3**

**Prerequisites**

Before you begin, make sure you have the following:

- An AWS account: Sign up for an AWS account if you don't have one already at [AWS Sign-Up](https://aws.amazon.com/).

**Step-by-Step Guide**

Follow these steps to host your static website on Amazon S3:

### **1. Create an S3 Bucket**

1.1. Log in to your AWS Console.

1.2. Navigate to the S3 service.

1.3. Click the "Create bucket" button.

1.4. Choose a unique bucket name and the AWS region closest to your target audience.

1.5. Leave the default settings for the rest of the options and click "Create bucket."

### **2. Upload Website Files**

2.1. In your S3 bucket, create the following folders if they don't exist: css, json, images, and js.

2.2. Upload all your website files and folders, including about.html, contact.html, index.html, service.html, and any other assets, to the respective folders.

### **3. Set Up a Bucket Policy**

3.1. In your S3 bucket, click on the "Permissions" tab.

3.2. Under "Bucket policy," click "Edit."

3.3. Add the following JSON policy, replacing your-bucket-name with your actual bucket name:

3.4. Save the bucket policy.

### **4. Enable Website Hosting**

4.1. In your S3 bucket, go to the "Properties" tab.

4.2. Click on "Static website hosting."

4.3. Choose "Use this bucket to host a website."

4.4. Set "Index document" to index.html or your desired default page.

4.5. Optionally, set the "Error document" if you have a custom 404 error page.

4.6. Save the changes.

### **5. Access Your Website**

5.1. After enabling website hosting, you'll see the endpoint URL. It should look like: http://your-bucket-name.s3-website-your-region.amazonaws.com.

5.2. You can access your website by opening this URL in a web browser.

**Support**

If you encounter any issues or have questions, feel free to [create an issue](https://github.com/your-repo/issues) in this repository for assistance.

Happy web hosting!

### **Custom Domain Configuration (Optional)**

If you want to use a custom domain for your static website hosted on Amazon S3, follow these additional steps:

#### **6. Configure a Custom Domain**

6.1. Purchase a domain name if you don't have one already. You can use services like AWS Route 53, GoDaddy, Namecheap, etc.

6.2. In your DNS settings, create a CNAME record or an alias record that points to your S3 bucket's website endpoint URL. This typically involves adding a record with the subdomain (e.g., www) and target the S3 endpoint URL.

#### **7. Enable SSL (Optional)**

If you want to secure your website with SSL (HTTPS), you can use AWS Certificate Manager to obtain a free SSL certificate.

7.1. In the AWS Certificate Manager, request a certificate for your custom domain. Follow the on-screen instructions to validate your domain ownership.

7.2. Once your certificate is issued, associate it with your CloudFront distribution.

#### **8. Configure CloudFront (Optional)**

To enhance website performance and use SSL, you can set up an Amazon CloudFront distribution in front of your S3 bucket.

8.1. Create a CloudFront distribution and configure it to use your S3 bucket as the origin.

8.2. Set up your SSL certificate if you have one.

8.3. Configure your domain to point to the CloudFront distribution.

Now, your website should be accessible using your custom domain via HTTPS.

**Contributing**

We welcome contributions to improve this guide. If you have any suggestions, corrections, or additional steps that could help users, please feel free to open a pull request on this repository.

**License**

This project is licensed under the MIT License. You are free to use, modify, and distribute it as needed.

**Acknowledgments**

Special thanks to the AWS documentation and the open-source community for providing resources and tools that make hosting static websites on S3 possible.

**Disclaimer**

Please note that AWS services may have associated costs. Make sure to monitor your usage to avoid unexpected charges.

Feel free to improve this README with more details, clarify steps, and add any specific instructions related to your website template if needed.
