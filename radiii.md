Name: IRADUKUNDA DEBORAH
ID: 29121

Oracle SQL Developer Installation Documentation (Ubuntu)
Prerequisites: Java Installation

Step A: Check Java Availability

java -version


Step B: Install Java (If Not Installed)

sudo apt update
sudo apt install openjdk-11-jdk -y


Step C: Confirm Java Installation

java -version

Oracle SQL Developer Setup
Step D: Download Oracle SQL Developer

Open a web browser

Go to: https://www.oracle.com/tools/downloads/sqldev-downloads.html

Accept the license agreement

Download the Linux (ZIP) version:
sqldeveloper-24.3.1.347.1826-no-jre.zip

Save the file to the Downloads directory

Step E: Extract the Downloaded File

Navigate to the Downloads directory:

cd ~/Downloads


Extract the ZIP file:

unzip sqldeveloper-24.3.1.347.1826-no-jre.zip

Step F: Move SQL Developer to Installation Directory
sudo mv sqldeveloper /opt/

Launching and Configuration
Step G: Run SQL Developer

Navigate to the SQL Developer directory:

cd /opt/sqldeveloper


Launch SQL Developer:

./sqldeveloper.sh

Step H: Java Path Configuration (First Launch Only)

Locate Java path:

readlink -f $(which java)


Provide Java home directory:

/usr/lib/jvm/java-11-openjdk-amd64

Desktop Launcher Creation
Step I: Create Application Launcher File
nano ~/.local/share/applications/sqldeveloper.desktop


Add the following configuration:

[Desktop Entry]
Version=1.0
Type=Application
Name=Oracle SQL Developer
Exec=/opt/sqldeveloper/sqldeveloper.sh
Icon=/opt/sqldeveloper/icon.png
Terminal=false
Categories=Development;

Step J: Save and Exit

Press Ctrl + X

Press Y

Press Enter

Git Workflow and Submission Repository Setup
Step K: Navigate to Working Directory
cd ~/Documents

Step L: Clone the Repository
git clone https://github.com/eliekayitare/PLSQL_SEM2_F.git

Branch Management
Step M: Create Branch
git branch IRADUKUNDA_DEBORAH_29121

Step N: Switch to the Branch
git checkout IRADUKUNDA_DEBORAH_29121

Making and Saving Changes
Step O: Modify Files

Open the project in an editor

Modify files as required

Save changes

Staging and Committing
Step P: Check Status
git status

Step Q: Stage Changes
git add .

Step R: Commit Changes
git commit -m "Branch Init"

Push to Remote Repository
Step S: Push Branch
git push -u origin IRADUKUNDA_DEBORAH_29121