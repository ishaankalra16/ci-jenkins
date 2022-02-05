####
### Vprofile-project

A demo application integrated, tested and analysed with the tools such as Jenkins, Nexus, SonarQube that send every notification to desired slack regarding every build of the pipeline. 

### Prerequisites
- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later

### Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL

### Architecture

<img width="685" alt="152109592-a3629c85-2562-4ca5-835e-fd6b39331b5d" src="https://user-images.githubusercontent.com/68735863/152641500-c9dceabf-9412-4da1-8c08-62d3b86196e7.png">

### Flow of Execution

- Login to AWS Console
- Create Login key pair for the EC2 Instances
- Create Security Group
  - Jenkins
  - Nexus
  - Sonarqube
- Create EC2 Instances with the userdata
  - Jenkins
  - Sonarqube
  - Nexus
- Configuring Jenkins and installing the required plugins
- Nexus Repository Setup
  - Release Version repository
  - Central repository for dependencies
  - Snapshot
  - Group repository 
- Sonarqube Post installation
- Jenkins Steps
  - Build Job
  - Setup Slack Notification
  - Checkstyle Code Analysis Job
  - Sonarqube Code Analysis Job
  - Artifact upload Job
- Connect all Jobs together with Build Pipeline
- Set Automatic Build Trigger
 
### Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql

### Screenshots

![Screenshot (342)](https://user-images.githubusercontent.com/68735863/152112558-f3ad4ea9-97e8-4869-a2b8-1590832d26f7.png)

![Screenshot (343)](https://user-images.githubusercontent.com/68735863/152110101-b51152c1-dcc9-4427-8187-e227a3f38054.png)

![Screenshot (344)](https://user-images.githubusercontent.com/68735863/152110116-dab57bc1-f8f0-4f8f-8c2c-626889607e78.png)

![Screenshot (345)](https://user-images.githubusercontent.com/68735863/152110138-246f6050-02f3-44e8-8662-95c09025c172.png)

![Screenshot (346)](https://user-images.githubusercontent.com/68735863/152110158-74ae59c6-5cc1-49f4-84aa-b9c8d8c3fd48.png)

![Screenshot (347)](https://user-images.githubusercontent.com/68735863/152113592-a7e0a440-d4e6-4cd7-831f-58251b17af2a.png)


