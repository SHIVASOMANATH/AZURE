# Task 1 spring pet clinic: 
---------------------------

Manual Build:
------------
*  sudo apt update
*  sudo apt install openjdk-17-jdk maven -y
*  git clone https://github.com/spring-projects/spring-petclinic.git
*  cd spring-petclinic
*  mvn package 

Pipeline:
---------
```yaml

trigger:
- main

pool:
  name: default
steps:
  - task: Maven@3
    inputs: 
      mavenPOMFile: 'pom.xml' 
      goals: 'package'
      publishJUnitResults: true 
      testResultsFiles: '**/surefire-reports/TEST-*.xml'
      testRunTitle: 'unittests'
```
![preview](/AZURE/images/4.PNG)

![preview](/AZURE/images/11.PNG)

# Task 2 Game of life:
---------------------------
      
Manual steps
------------
- sudo apt install openjdk-8-jdk
- sudo apt install maven 
- git clone https://github.com/wakaleo/game-of-life.git
- cd gol
- mvn package
---
Pipeline:
---------
```yaml
trigger:
  - master
  
pool:
  name: default

jobs:
  - job: buildjob
    displayName: Build and Package Game of life
    steps:
      - task: Maven@3
        inputs:
          mavenPOMFile: 'pom.xml'
          goals: 'package'
          publishJUnitResults: true
          testResultsFiles: '**/surefire-reports/TEST-*.xml'
```

![preview](/AZURE/images/6.PNG)

![preview](/AZURE/images/10.PNG)

# Task 3 Nop Commerce:
----------------------
      
Manual steps
------------
* sudo apt update
* git clone https://github.com/nopSolutions/nopCommerce.git
* git checkout master
* cd nopCommerce/
* git checkout master
* dotnet restore src/NopCommerce.sln
* dotnet build src/NopCommerce.sln

![preview](/AZURE/images/7.PNG)

Pipeline:
---------
```yaml

trigger:
  - master

pool:
  vmImage: 

steps: 
  - task: DotNetCoreCLI@2 
    inputs: 
      command: 'restore'
      projects: src/NopCommerce.sln
  - task: DotNetCoreCLI@2 
    inputs: 
      command: 'build'
      projects: src/NopCommerce.sln

```
![preview](/AZURE/images/9.PNG)

![preview](/AZURE/images/8.PNG)

