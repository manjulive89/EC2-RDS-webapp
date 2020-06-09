# EC2-RDS-webapp
This AWS CloudFormation Template will launch an Amazon EC2 instance of type t2.micro with latest Amazon Linux 2 OS, bootstrap Apache/PHP, and install a simple address book web application. The template will also create an Amazon RDS MySQL database instance in free tier, i.e. of type db.t2.micro and with no Multi-AZ setup or read replicas. The WebTier Security Group will allow only SSH and HTTP connections to this web server EC2 instance, and the DBTier Security Group will only allow the WebTier Security Group to initiate database connections to the RDS DB instance over TCP port 3306. 

# Pre-requistes
Create a EC2 Key pair and save the private key. EC2 Key Pairs are used to connect securely to your EC2 Linux-based instances using SSH. 
