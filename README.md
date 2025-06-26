<h1>🚀 Terraform AWS Project | VPC | EC2 | ALB | IGW | Route Table 🌐</h1>

<p><img src="https://img.shields.io/badge/Terraform-IaC-blueviolet?logo=terraform">
<img src="https://img.shields.io/badge/AWS-Cloud-orange?logo=amazon-aws">
<img src="https://img.shields.io/badge/License-MIT-green">
<img src="https://img.shields.io/badge/Status-Active-brightgreen"></p>

<hr>

<h2>📚 Overview</h2>

<p>This project uses <strong>Terraform</strong> to deploy a simple, scalable, and highly available AWS infrastructure that includes:</p>

<ul>
    <li>✅ <strong>VPC</strong></li>
    <li>✅ <strong>Internet Gateway</strong></li>
    <li>✅ <strong>2 Public Subnets (in different AZs)</strong></li>
    <li>✅ <strong>Route Table with Internet Gateway association</strong></li>
    <li>✅ <strong>2 EC2 Instances (Web Servers)</strong></li>
    <li>✅ <strong>Application Load Balancer (ALB)</strong></li>
</ul>

<hr>

<h2>📌 Architecture Diagram</h2>

<pre>
[Internet]
    |
[Internet Gateway]
    |
[ALB (HTTP Load Balancer)]
    |
  /   \
[EC2-1] [EC2-2]
 (Subnet-1) (Subnet-2)
</pre>

<hr>

<h2>📁 Project Structure</h2>

<pre>
Terraform_Aws_Project/
├── main.tf          # Main Terraform configuration file
├── outputs.tf       # Outputs such as Load Balancer DNS
├── variables.tf     # (Optional) Input variables
├── README.md        # This file
</pre>

<hr>

<h2>🚀 Deployment Steps</h2>

<details>
<summary>⚙️ <b>Pre-requisites</b> (Click to expand)</summary>
<ul>
    <li>AWS CLI installed and configured (<code>aws configure</code>)</li>
    <li>Terraform installed → <a href="https://developer.hashicorp.com/terraform/downloads">Download Terraform</a></li>
    <li>An AWS EC2 Key Pair for SSH access to instances</li>
</ul>
</details>

<details>
<summary>🚀 <b>Deployment Instructions</b> (Click to expand)</summary>

<h3>1️⃣ Clone the repository</h3>
<pre><code>git clone https://github.com/rakeshmiriyala/Terraform_Aws_Project.git
cd Terraform_Aws_Project</code></pre>

<h3>2️⃣ Initialize Terraform</h3>
<pre><code>terraform init</code></pre>

<h3>3️⃣ Validate configuration</h3>
<pre><code>terraform validate</code></pre>

<h3>4️⃣ Apply configuration</h3>
<pre><code>terraform apply</code></pre>

<p>➡️ Confirm with <code>yes</code> when prompted.</p>

<p>✅ After deployment, the Load Balancer DNS will be displayed in the output.</p>

</details>

<hr>

<h2>🧱 AWS Resources Created</h2>

<table>
    <thead>
        <tr>
            <th>Resource</th>
            <th>Count</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>VPC</td><td>1</td><td>Custom Virtual Private Cloud</td></tr>
        <tr><td>Internet Gateway</td><td>1</td><td>Enables internet access</td></tr>
        <tr><td>Public Subnets</td><td>2</td><td>Located in different Availability Zones</td></tr>
        <tr><td>Route Table</td><td>1</td><td>With route to Internet Gateway</td></tr>
        <tr><td>EC2 Instances</td><td>2</td><td>Web Servers (Apache installed)</td></tr>
        <tr><td>Application Load Balancer</td><td>1</td><td>HTTP Load Balancer distributing traffic</td></tr>
        <tr><td>Security Groups</td><td>2</td><td>For ALB and EC2 (HTTP & SSH)</td></tr>
    </tbody>
</table>

<hr>

<h2>🌐 Access Load Balancer</h2>

<p>After successful deployment, open the Load Balancer DNS URL in a browser:</p>

<pre><code>http://&lt;LoadBalancer-DNS-Name&gt;</code></pre>

<p>✔️ You should see web pages from both EC2 instances:</p>

<ul>
    <li>Web Server 1 - &lt;hostname&gt;</li>
    <li>Web Server 2 - &lt;hostname&gt;</li>
</ul>

<hr>

<h2>🧹 Destroy Infrastructure</h2>

<p>To remove all the resources created by Terraform:</p>

<pre><code>terraform destroy</code></pre>

<hr>

<h2>🔧 Customization</h2>

<ul>
    <li>✔️ Change the AMI ID based on your AWS region (Update in <code>main.tf</code>)</li>
    <li>✔️ Update your key pair name (<code>key_name</code>) for SSH access</li>
    <li>✔️ Extend the setup by adding:
        <ul>
            <li>Private Subnets</li>
            <li>NAT Gateways</li>
            <li>Auto Scaling Groups</li>
            <li>RDS databases</li>
        </ul>
    </li>
</ul>

<hr>

<h2>👨‍💻 Author</h2>

<ul>
    <li><strong>Rakesh Miriyala</strong></li>
    <li><a href="https://github.com/rakeshmiriyala">GitHub → rakeshmiriyala</a></li>
</ul>

<hr>

<h2>📜 License</h2>

<p>This project is licensed under the <strong>MIT License</strong>. See the <code>LICENSE</code> file for more details.</p>

<hr>

<h2>⭐️ Support</h2>

<p>If you found this project helpful, consider giving it a ⭐️ on <a href="https://github.com/rakeshmiriyala/Terraform_Aws_Project">GitHub!</a></p>

<h2>🚀 Happy Terraforming! 🚀</h2>
