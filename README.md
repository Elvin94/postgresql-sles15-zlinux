# postgresql-sles15-zlinux
Install and deploy postgresql database on Linux on z


## Prerequisites
 1. Request access to LinuxONE Community Cloud. Follow instructions [here](https://github.com/Elvin94/LinuxONE-OSS-CC)

## Hardware requirements
1. SLES15 SP2
### Step 1: Install postgres database server on LinuxONE Community Cloud
   1.1 Import postgres package
   ```sh
   rpm --import http://packages.2ndquadrant.com/postgresql-z/RPM-GPG-KEY-2NDQ-RHEL7
   ```
    
   1.2 Configure yum repo
   ```sh
   yum-config-manager --add-repo http://packages.2ndquadrant.com/postgresql-z/yum/12/rhel7-s390x
   ```
   1.3 Install postgresql
   ```sh
   sudo yum install postgresql-server
   ```
   
   
   ### Step 2: Configure Postgresql server
   
   2.1 Start postgresql service
   ```sh
   sudo system start postgresql.service 
   ```
   2.2 Enable postgres
   ```sh
  sudo system enable postgresql.service 
   ```
   2.3 Check status of the postgresql server
   ```sh
   sudo systemctl status postgresql.service 
   ```
   
   Optional - Output should look like this
   
   ![alt text](images/configs.png "Check /data disk")
   
    
