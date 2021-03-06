## Instructions for Task #1 ##
 
The `python-test1.py` is python3 based and can be ran using following command :

    ```
    python3 python-test1.py
    ```
The program will ask for number of rows as input, if no input is given default will be taken as `6`. As `6` rows for the pyramid pattern.

Enter number of rows or press simply enter, will provide following output :
    ```
    Program to print half pyramid:
    Enter number of rows:
    *
    * * *
    * * * *
    * * * * * *
    * * * * * * *
    * * * * * * * * *
    ```
## Instructions for Task #2 ##    

The ansible playbook for deploying Tomcat Server. The playbook is written compatible with ansible-2.4.x available in centos7 repo.

To deploy tomcat server, run following command :

    ```
    ansible-playbook -v app-deploy.yml
    ```

Once the deployment complete the tomcat server UI is avaible at http://localhost:8000, to access Manager App UI user `admin/secret123` credentials. 

The playbook is flexible of installing tomcat server instances on same machine. Use `vars-2.yml` instead on `vars.yml` to deploy another instance of tomcat on same VM at different location and port number.

    ```
    mv vars-2.yml vars.yml
    ```
To access ServerB  http://localhost:8001, to access Manager App UI user `admin/pass123` credentials. 

## Instructions for Task #3 ##

Add `jenkins` user to sudoers file.

```
jenkins         ALL=(ALL)       NOPASSWD: ALL
```
Copy Jenkinfile in the repo to pipeline script, this will  deploy above playbook via jenkins pipeline.

Click `Build now` to run job. This will deploy tomcat on local system and can be accessible via http://localhost:8000.

## Instructions for Task #4 ##

`HA-App-design.pdf` added in the repository which explains, architecture Model for a high availability Three tier application in AWS.
