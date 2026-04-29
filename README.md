✅ PART 1 – LINUX COMMANDS (Minimum 10)
Open Git Bash.

1️⃣ Check present directory
Bash

pwd
2️⃣ List files
Bash

ls
3️⃣ Create folder
Bash

mkdir DevOpsLab
4️⃣ Go inside folder
Bash

cd DevOpsLab
5️⃣ Create file
Bash

touch file1.txt
6️⃣ Write inside file
Bash

echo "DevOps Practical" > file1.txt
7️⃣ View file
Bash

cat file1.txt
8️⃣ Copy file
Bash

cp file1.txt file2.txt
9️⃣ Rename file
Bash

mv file2.txt renamed.txt
🔟 Delete file
Bash

rm renamed.txt
✅ Linux part done.

✅ PART 2 – GIT COMPLETE FLOW (Proper Clean Method)
✅ Step 1: Go to Home
Bash

cd ~
✅ Step 2: Create New Project
Bash

mkdir DevOpsGitLab
cd DevOpsGitLab
✅ Step 3: Configure Git (VERY IMPORTANT)
Bash

git config --global user.name "JaansPravin"
git config --global user.email "yourgithubemail@gmail.com"
Check:

Bash

git config --list
✅ Step 4: Initialize Git
Bash

git init
✅ Step 5: Create File
Bash

touch index.html
echo "<h1>DevOps Exam</h1>" > index.html
✅ Step 6: Check Status
Bash

git status
✅ Step 7: Add File
Bash

git add .
✅ Step 8: Commit
Bash

git commit -m "Initial commit"
✅ Step 9: Check Branch
Bash

git branch
If shows:

text

* master
Rename it:

Bash

git branch -M main

✅ PART 3 – CONNECT TO GITHUB
✅ Step 1: Create Repo on GitHub
Go to GitHub → New Repository
Name: DevOpsGitLab
Do NOT add README.

✅ Step 2: Add Remote
Bash

git remote add origin https://github.com/JaansPravin/DevOpsGitLab.git
Check:

Bash

git remote -v
✅ Step 3: Push
Bash

git push -u origin main
When asked:

Username:

text

JaansPravin
Password:
👉 Paste Personal Access Token

✅ Done.

✅ PART 4 – MODIFY + PUSH AGAIN
Bash

echo "<p>Updated</p>" >> index.html
git add .
git commit -m "Updated file"
git push
✅ PART 5 – PULL / FETCH / MERGE
Pull
Bash

git pull origin main
Fetch
Bash

git fetch

Merge
Bash

git merge origin/main
✅ Git part complete.

✅ PART 6 – DOCKER COMMANDS (Minimum 10)
Make sure Docker Desktop is running.

1️⃣ Check version
Bash

docker --version
2️⃣ Check running containers
Bash

docker ps
3️⃣ Check all containers
Bash

docker ps -a
4️⃣ Pull image
Bash

docker pull nginx
5️⃣ List images
Bash

docker images
6️⃣ Run container
Bash

docker run -d -p 8080:80 nginx
7️⃣ Check running
Bash

docker ps
Open browser:

text

localhost:8080
8️⃣ Stop container
Bash

docker stop <container_id>
9️⃣ Remove container
Bash

docker rm <container_id>
🔟 Remove image
Bash

docker rmi nginx
✅ 10 Docker commands done.

✅ PART 7 – DOCKERFILE (Image Build)
Inside folder:

Bash

touch Dockerfile
Add content:

Bash

echo "FROM nginx" > Dockerfile
Build image:

Bash

docker build -t mynginx .
Run:

Bash

docker run -d -p 8081:80 mynginx

✅ PART 6 – DOCKER COMMANDS (Minimum 10)
Make sure Docker Desktop is running.

1️⃣ Check version
Bash

docker --version
2️⃣ Check running containers
Bash

docker ps
3️⃣ Check all containers
Bash

docker ps -a
4️⃣ Pull image
Bash

docker pull nginx
5️⃣ List images
Bash

docker images
6️⃣ Run container
Bash

docker run -d -p 8080:80 nginx
7️⃣ Check running
Bash

docker ps
Open browser:

text

localhost:8080
8️⃣ Stop container
Bash

docker stop <container_id>
9️⃣ Remove container
Bash

docker rm <container_id>
🔟 Remove image
Bash

docker rmi nginx
✅ 10 Docker commands done.

✅ PART 7 – DOCKERFILE (Image Build)
Inside folder:

Bash

touch Dockerfile
Add content:

Bash

echo "FROM nginx" > Dockerfile
Build image:

Bash

docker build -t mynginx .
Run:

Bash

docker run -d -p 8081:80 mynginx
✅ PART 8 – JENKINS BASIC FLOW
In browser:

text

localhost:8080
✅ Create New Item
New Item
Freestyle Project
✅ Source Code Management
Git
Paste GitHub repo URL
✅ Build Step
For Java:

text

javac Hello.java
java Hello
For Python:

text

python script.py
✅ Build Now
✅ If Asked: Pipeline Script
groovy

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building project'
            }
        }
    }
}
