pipeline{
    agent any
    stages{
        stage("STAGE 1 checkout the git code"){
            steps{
                echo "git checkout started"
                git url: "https://github.com/akshu20791/DevOpsClassCodes"
                echo "git checkout done"
            }
        }
        stage("STAGE 2 compiling the code"){
            steps{
                echo "compiling the code started"
                sh "mvn compile"
                echo "compiling done"
            }
        }
        stage("STAGE 3 testing the code by akshat"){
            steps{
                echo "testing the code"
                sh "mvn test"
            }
        }
        stage("STAGE 4 Quality assurance of the code"){
            steps{
                echo "checking the quality of the code"
                sh "mvn checkstyle:checkstyle"
            }
        }
        stage("STAGE 5 packaging the code"){
            steps{
                echo "packaging the code"
                sh "mvn package"
            }
        }
        stage("STAGE 6 deploy the project"){
            steps{
                sh "sudo cp -f /var/lib/jenkins/workspace/pipeline/target/addressbook.war /opt/apache-tomcat-8.5.100/webapps"
            }
        }
    }
}
