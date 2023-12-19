pipeline {

    tools {
        maven "maven"
        jdk "jdk17"
    }

    stages {
        stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /var/lib/jenkins/apache-maven*"
            }
        }
        stage('Build') {
            steps {
                dir("/var/lib/jenkins/workspace/maven-sample-project/my-app") {
                sh 'mvn clean package'
                }
            
            }
        }
     }
}
