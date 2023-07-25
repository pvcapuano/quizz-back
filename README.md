```
CREATE DATABASE IF NOT EXISTS QuizDB;
USE QuizDB;

-- Criação da tabela Questions
CREATE TABLE IF NOT EXISTS Questions (
    QnId INT AUTO_INCREMENT PRIMARY KEY,
    QnInWords NVARCHAR(250) NOT NULL,
    ImageName NVARCHAR(50),
    Option1 NVARCHAR(50) NOT NULL,
    Option2 NVARCHAR(50) NOT NULL,
    Option3 NVARCHAR(50) NOT NULL,
    Option4 NVARCHAR(50) NOT NULL,
    Answer INT NOT NULL,
    CONSTRAINT UQ_QnInWords UNIQUE (QnInWords)
);

-- Inserção de uma pergunta de exemplo
INSERT INTO Questions (QnInWords, ImageName, Option1, Option2, Option3, Option4, Answer)
VALUES 
(N'Why is AWS more economical than traditional data centers for applications with varying compute workloads?', NULL, N'Amazon Elastic Compute Cloud costs are billed on a monthly basis.', N'Customers retain full administrative access to their Amazon EC2 instances.', N'Amazon EC2 instances can be launched on-demand when needed.', N'Customers can permanently run enough instances to handle peak workloads.', 2),
(N'Which AWS service would simplify migration of a database to AWS?', NULL, N'AWS Storage Gateway', N'AWS Database Migration Service', N'Amazon Elastic Compute Cloud', N'Amazon AppStream 2.0', 1),
(N'Which AWS offering enables customers to find, buy, and immediately start using software solutions in their AWS environment?', NULL, N'AWS Config', N'AWS OpsWorks', N'AWS SDK', N'AWS Marketplace', 3),
(N'Which AWS networking service enables a company to create a virtual network within AWS?', NULL, N'AWS Config', N'Amazon Route 53', N'AWS Direct Connect', N'Amazon Virtual Private Cloud', 3),
(N'Which of the following is AWSs responsibility under the AWS shared responsibility model?', NULL, N'Configuring third-party applications', N'Maintaining physical hardware', N'Securing application access and data', N'Managing custom Amazon Machine Images AMIs', 1),
(N'Which component of AWS global infrastructure does Amazon CloudFront use to ensure low-latency delivery?', NULL, N'AWS Regions', N'AWS Edge Locations', N'AWS Availability Zones', N'Amazon Virtual Private Cloud', 1),
(N'How would a system administrator add an additional layer of login security to a users AWS Management Console?', NULL, N'Use AWS Cloud Directory', N'Audit AWS Identity and Access Management (IAM) roles', N'Enable Multi-Factor Authentication', N'Enable AWS CloudTrail', 2),
(N'Which service can identify the user that made the API call when an Amazon Elastic Compute Cloud (Amazon EC2) instance is terminated?', NULL, N'Amazon CloudWatch', N'AWS CloudTrail', N'AWS X-Ray', N'AWS Identity and Access Management', 1),
(N'Which service would you use to send alerts based on Amazon CloudWatch alarms?', NULL, N'Amazon Simple Notification Service', N'AWS CloudTrail', N'AWS Trusted Advisor', N'Amazon Route 53', 0),
(N'Where can a customer find information about prohibited actions on AWS infrastructure?', NULL, N'AWS Trusted Advisor', N'AWS Identity and Access Management', N'AWS Billing Console', N'AWS Acceptable Use Policy', 3);

```
