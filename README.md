## 1 - Create pipeline Jenkins job for golang project

### Install Go Plugin

1) Go to **Manage Jenkins** -> **Manage Plugins**
2) Select Available plugins and search **Go**, check install and click **Install without restart**

### Add Go Installation

1) Go to **Manage Jenkins** -> **Global Tool Configuration**
2) Find **Go** section and click Add **Go**
3) Add name for Go installation, check **Install automatically**, choose Go version and **Save** changes

### Create Jenkins pipeline job
    
1) Create Jenkinsfile on Repository and add pipeline code inside
2) Go to **Jenkins Dashboard** and click **New Item**, enter Item Name and choose **Pipeline**
3) In Pipeline section select **Pipeline script from SCM** and choose **Git**
4) Provide Repository URL and Credentials created in previous steps, and select which Branch to build and fill Script path with path to Jenkinsfile on Repository
5) **Save** changes and click **Build now**
