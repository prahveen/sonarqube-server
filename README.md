## Prerequisites 
    * Install docker
    * Install java

## Setup SonarQube Server
    clone this repo and run below command
    ```
        $ docker-compose up -d
    ```
    Once you done with above command, you can access the sonar qube server on http://localhost:9000,
    
### Defualt Credetials
    ```
        username: admin
        password: admin
    ```

## How To Run Sonar Scanner
    * Download [sonnar scanner cli] (https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/)
    * Create sonar-project.properties file in root of the project
        ```
            sonar-project.properties
            sonar.projectKey=owner-app
            sonar.sources=.
            sonar.language=ts
            sonar.exclusions=node_modules
            sonar.eslint.reportPaths=lint-report.json

            sonar.host.url=http://localhost:9000
            sonar.login=ff4d45d148eed652f85c0b8fed5ca64c1a28179f
        ```
    * Run sonnar scanner command in root of the project directory
        ```
            $ _path_to_downloaded_cli\bin\sonar-scanner
        ```



