#### 04-07-2023
- CI(Integration) /CD(Delivery)/CD (Deployement)
- CI/CD  Call the tool work to doo
- Rasberry PI///
- Vcs- Git
- Build Package- Maven/MS build/Docker
- ST env
- PT env
- Deployements- Kubernetes and ansible Terraform
- PreProf env
- Pipeline_- AzureDevOps
- Build Package - Docker

- Azure DevOps are widely used pipeline tool that the cause we are knowing about it

# - Big bang integration
- waterfall model --- Req -design- Devlopment- testing - Deployement- Mainatainance
- these are error prone
- CI - Inform the failure on integrations
- cruise controll -- hatsun-- jenkins\
- AGILE -- Toyoto  Relay rase concept
- Automated pipe line which devoper push the change
- Build -package
- code quality 
- system perfermance reliabilty security
- report the Quantity 
- cant be graterthen 1 month
-  Git 
- Yaml (declarative Aaproches)
- Azure DevOps
    - Boards
    - Build & Releases pipe line
    - Artifacts
    - Documentations
    - Azure source Repos\
- Code Bases
 

- Vcs-- Build package-- Run unit test -- Static Code Analysis -- Depoly into ST ENV+Run Automated tests - Depoly into PT ENV+Run Automated tests

- Git
-----
* distributed vcs
- hosted manu providers
  - Git hub
  - azure source repos
  - code commit
  - git bucket
  - Git lab
- Vcs client
- Vcs server 
- Vcs server 

#  Gol Installation (WOW) 
- Manual steps
- Implement install manual steps pipe line ci/cd
- steps for gameoflife
- software required
  - git 
  - jdk8
  - mvn
  
# BASICS:
- git pull
- git push - u origin /master
- git clone 
- git add .
- git status
- git commit -m "name"
- git config
- git branch -r 
- git remote

* Default branch: master
* Default remote: origin
- we can work with multiple origins and branches
- 

Build and Package code:
----------------------- 
- programing languages are categorixed 3 formates
 - compiler based: C language ,windows,,mac >> linux compiler its like to be dubbing langufa formate
 - interpreter based: eg: translater in meet  interpeter need to be installed in our system
 - Hybrid : 
- compile based: 

- java >>complie>>  byte code>>  (jar,war,tar) --openjdk
- c# il (intermediate language)>>complie>> >> .net core ----maven ( exe,dll)
--- sdk (software devolpment kit)
-- Fast api

# session 2:

### Dependecy Managment:
------------------------
- lots of dependecies are availble reusable
- we need to download dependencies 
   - nodejs `npm `
   - pytho `pip`
   - .net `nuget`
   - java `maven`

- unit test: using code we are verified the process called unit test
  - api testing ... deskotp required... not required

- Functional tests:
 - automation test: selenium ,,
 - ui tests (simualte user) ,
 - sdks 
 - api tests (postman,rest assured)
- performance tests:
  - load testing harness(j meter ,load runner)
- result required : juint xml formate


## Java Based Aplication
-----------------------
 - ANT
 - Maven
 - Gradle

wee need 
 - Java 17
 - Mave 3
 - project -  spring petclinic

spring pet clinic:

*  sudo apt update
*  sudo apt install openjdk-17-jdk maven -y
*  git clone https://github.com/spring-projects/spring-petclinic.git
*  cd spring-petclinic
*  mvn package # creates package, run unit tests
 - clasic .net -- windows
 - dontnet core - linux,windows

### Azure DevOps
----------------
 - VSTS : visual studio team services microsoft
  - projrct Management
     - agile boards
     - issue tracker
  -  Execution
     - wiki Pages
     - Test Management
  - DevOps:
     - pipelines:
        - build pipelines & release
  - VCS:
      - Azure Source Repos
          - git 
          - tfvc -team foundation version controll 
  - 
low price to custamers

### Git workflow
-----------------
- create repostitory
- cloning local
- 

### Yaml Schema:
-----------------
- pipelines:
   - Trigger
     - Stage 
       - Agent - job - tasks
          - steps
              
-  executable plays : agents 
-  when execute: Trigger
   -  stages
   -  extends : reusblity
   -  jobs
   -  steps
        - task: 

### self Hosted agents 
----------------------

### Microsoft Hosted agents
-----------------------------

```yaml
steps: 
- task: 
  inputs:
    mavenPomFile: 'pom.xml'
    goals: 'package'
```
# Date 26-6-2023
-----------------
-  Agents
   - microsoft hosted : `2 vcpu and 8 GB RAM`
    - Self Hosted: 
      - our convinient uses select and configure 
      -  
Dev>> Build >> test >> Artfacts (result of what we build) >> Deployments >> 
 
Dev>> Build >> test >> Artfacts (result of what we build)  Build pipeline>>>

Artfacts (result of what we build) >> Deployments >>  Release pipe line

   - new repository Ad
   - ssh 
   - my id-rsa
   - repo >> git hub>> 
  -  local disk
   - git clone spc
   - cd spc
  - add to Az
  - copy ssh
  - git branch
  - git remote add spc git@ssh.dev.azure.com:v3/shivasomanath7/project/springpetclinic
  - git push spc main
  cli based add azuredevops
![preview](/AZURE/images/1.PNG)

- Self host agent 

spc
  - vm 
  - install jdk 17 
  - install maven
``` 
sudo apt update 
sudo apt install openjdk-17-jdk maven -y
```
   - project settings
   - agent pools

``` 
- wget download agent from default agent (https://vstsagentpackage.azureedge.net/agent/3.220.5/vsts-agent-linux-x64-3.220.5.tar.gz)
- copy the code from new agent cretion path 
- Create the agent
~/$ mkdir myagent && cd myagent
~/myagent$ tar zxvf ~/vsts-agent-linux-x64-3.220.5.tar.gz
- Configure the agentDetailed instructions
~/myagent$ ./config.sh
- Optionally run the agent interactively
  If you didn't run as a service above:
~/myagent$ ./run.sh

M2_HOME='/opt/apache-maven-3.9.3'
PATH="$M2_HOME/bin:$PATH"
export PATH

export PATH="/opt/maven/apache-maven-3.9.3/bin:$PATH"


```
![preview](/AZURE/images/5.PNG)


- credentials:

   - tzeqayseikrhenjywogfpw3gcgnbcifr72z4f23ddtz2auohtlgq token created hosts
   - url https://dev.azure.com/shivasomanath7

- gmu76ygmmtbqo2wmivelzbettml5o3zcnjfv4zif5j5ax3ecblnq

![preview](/AZURE/images/2.PNG) Agent Configured


Pipeline configure:

setup build:
- statrtup pipeline
- yaml
- write pipe line
- 

![preview](/AZURE/images/3.PNG)

Date: 28-06-2023
-----------------
- Azure devops pipeline yaml schema
  - Tasks- predifined tasks
  - Market place (extention for Azure devops)
  - scripts
  - powershell pwsh shell

installl spring petclinic

- using bash
```yaml

trigger:
- main

pool:
  name: default
steps:
  - bash: printenv

```
- using tasks
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

[label](../springpetclinic/azure-pipelines.yml)
```yaml
trigger:
- main

pool:
  name: default

steps:
  - task: Maven@3
    inputs:
      mavenPOMFile: 'pom.xml'
      publishJUnitResults: true
      testResultsFiles: '**/surefire-reports/TEST-*.xml'
      jdkVersionOption: 'default'
      jdkDirectory:  /usr/share/java/
      mavenDirectory: /opt/maven
```
### 30-06-2023
---------------
- Azure pipeline using tasks
  - tasks: Maven@3
- Microsoft hosted agent : 2vcpu 8 gb
  - 
### Game Oflife  

```yaml
trigger:
- master

pool:
  name: default

steps:
  - task: Maven@3
    inputs:
      mavenPOMFile: 'pom.xml'
      goals: package
      publishJUnitResults: true
      testResultsFiles: '**/surefire-reports/TEST-*.xml'
    - task: CopyFiles@2
      inputs:
        Contents: "**/target/gameoflife.war"
        TargetFolder: $(Build.ArtifactStagingDirectory)
    - task: PublishBuildArtifacts@1
      inputs:
        pathToPublish: $(Build.ArtifactStagingDirectory)
        artifactName: Gameoflifeartifacts

```


![preview](/AZURE/images/6.PNG)


![preview](/AZURE/images/10.PNG)

variables:
    predefined varibales:
            - task: CopyFiles@2
        inputs:
          Contents: "**/target/gameoflife.war"
          TargetFolder: $(Build.ArtifactStagingDirectory)
used for copy files one location to amnopther location 
publish build aratifacts: 
  - task: PublishBuildArtifacts@1
  inputs:
    pathToPublish: $(Build.ArtifactStagingDirectory)
    artifactName: GameoflifeArtifacts

Download artifacts:



### Manual steps

- check git/jdk/mvn
- sudo apt install openjdk-8-jdk
- sudo apt install maven 
- git clone https://github.com/wakaleo/game-of-life.git
- cd gol
- mvn package
- package location cd gameoflife-web/target (gameoflife.war)


 export JAVA_HOME="/usr/lib/jvm/java-8-openjdk-amd64/"
- `u7b2xrbo5wvttuwag4g7hloxkafj55fqelbo56gmfcmuiiu4o2vq`

### Manual steps ### Nop Commerce  

### For .net application
---------------------------
* sudo apt update
* git clone https://github.com/nopSolutions/nopCommerce.git
* git checkout master
* cd nopCommerce/
* git checkout master
* dotnet restore src/NopCommerce.sln
* dotnet build src/NopCommerce.sln

![preview](/AZURE/images/7.PNG)

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


Azure Devops Varibles:
----------------------
- environmental varible
- user defined
  - our vaibles
  variables:
  string: string # Name/value pairs

  pramaeters: canbe set during the time of execution also

  - name: mavenGoal
    displayName: Maven Goal
    type: string
    default: package
    values:
      - package
      - clean package
      - clean install
      - install

```yaml
trigger:
  - master
varibales:
  goals: package

parameters:
  - name: 
    displayname: 
    type: 
    default: 
    
pool:
  name: default

steps:
  - task: Maven@3
    inputs:
      mavenPOMFile: 'pom.xml'
      goals: ${goals}
      publishJUnitResults: true
      testResultsFiles: '**/surefire-reports/TEST-*.xml'
      javaHomeOption: 'JDKVersion'
      jdkVersionOption: '1.17'
    - task: CopyFiles@2
      inputs:
        Contents: "**/target/gameoflife.war"
        TargetFolder: $(Build.ArtifactStagingDirectory)
    - task: PublishBuildArtifacts@1
      inputs:
        pathToPublish: $(Build.ArtifactStagingDirectory)
        artifactName: Gameoflifeartifacts

```

Reusable Pipeline Using Templates:
-----------------------------------
use genric.yaml


```yaml
parameters:
- name: java-version
  type: string
  default: '1.11'
- name: mavenGoal
  type: string
  default: package
- name: artifactpath
  type: string
  default: '**/*.jar*'
- name: artifactName
  type: string
  default: generic

steps:

steps:
- task: Maven@3
  inputs:
    mavenPOMFile: 'pom.xml'
    goals: ${goals}
    publishJUnitResults: true
    testResultsFiles: '**/surefire-reports/TEST-*.xml'
    javaHomeOption: 'JDKVersion'
    jdkVersionOption: ${{ prameters.java-version }}
  - task: CopyFiles@2
    inputs:
      Contents: ${{ parameters.artifactpath }}
      TargetFolder: $(Build.ArtifactStagingDirectory)
  - task: PublishBuildArtifacts@1
    inputs:
      pathToPublish: $(Build.ArtifactStagingDirectory)
      artifactName: ${{ parameters.artifactName }}


```
pipelines ...
 Resources:

resources:
WW
```yaml

trigger:
  - main

pool:
  vmImage: ubuntu-22.04

resources:
  repositories:
    - repository: BuildTemplates
      name: BuildTemplates
      type: git

extends:
  template: generic-maven.yaml@BuildTemplates
  prameters:
        java-version: '1.8'
        mavenGoal: 'package'
        artifactpath: '**/target/gameoflife.war'
        artifactName: 'Gameoflifeartifacts''
      