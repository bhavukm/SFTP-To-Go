# SFTP-To-Go
SFTP-To-Go

**SFTP To Go:** https://sftptogo.com/

**Free Trial:** https://sftptogo.com/pricing

<img width="1536" height="1024" alt="SFTP To Go_1" src="https://github.com/user-attachments/assets/f20056af-39bd-40c4-a820-da921a5a9c05" />

**SFTP To Go** is a simple and secure cloud storage service. It lets you upload, download, and manage files using common protocols like SFTP, FTPS, Amazon S3, and HTTPS. You don’t need to set up or maintain any servers. Everything runs on AWS, so it’s fast, reliable, and 

scales automatically.

Businesses use SFTP To Go to safely exchange files with clients, vendors, and partners. You get secure access without worrying about infrastructure.

The platform is built for quick setup. You can manage users and files through a clean, easy dashboard. If you want to automate things, you can also use their APIs and webhooks to connect SFTP To Go with your applications.

If you ever need help, their support team is available through the chat option on the website.

**What is SFTP?**

**SFTP (SSH File Transfer Protocol)** is a secure file transfer protocol that runs over SSH.

Think of it as a file transfer built into SSH. If you can SSH into a server, you can usually use SFTP.

**Key points:**

Uses SSH (port 22)

Encrypts everything: authentication, commands, and data

Uses a single connection

Authenticates using SSH keys or passwords

Very common in Linux and cloud environments

**Real-world use:**

Uploading files to Linux servers

CI/CD pipelines pulling or pushing artifacts

Secure automation scripts in DevOps and SRE setups

**What is FTPS?**

**FTPS (FTP Secure)** is the traditional FTP protocol enhanced with TLS/SSL encryption.

It is basically FTP plus security.

**Key points:**

Uses FTP + TLS/SSL

Encrypts credentials and data

Uses multiple ports (control + data channels)

**Two modes:**

Explicit FTPS (client asks for encryption)

Implicit FTPS (encryption enforced from the start)

Relies on certificates

**Real-world use**

Enterprises with legacy FTP systems

Organizations already using PKI and certificates

Scenarios where FTP compatibility is required

**Commands used to run benchmark tests:**

mkdir sftpus

cd sftpus/

git clone https://github.com/crazyantlabs/sftp-ftps-benchmarks.git

cd sftp-ftps-benchmarks/

ll

chmod 777 *

cat > .env

./setup.sh

ps -ef | grep run-tests.sh

./generateFiles.sh ~/benchmarks/10MB 10 MB 10

./generateFiles.sh ~/benchmarks/10MB 100 MB 10

./generateFiles.sh ~/benchmarks/10MB 100 KB 10

./generateFiles.sh ~/benchmarks/10MB 1000 KB 10

./generateFiles.sh ~/benchmarks/20_5MB 5 MB 20

ln -s ~/benchmarks ./benchmarks

CURL_OPTS="--ftp-ssl --ftp-pasv --ftp-create-dirs -v"

nohup bash ./run-tests.sh  > output.log 2>&1

cat output.log

ll ~/benchmarks/
