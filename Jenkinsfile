pipeline {
    agent { label 'node1' } 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
        }
        stage('Stage 2') {
            steps {
                sh  """
                   cd /home/ec2-user/node1-slave/workspace/pipelinejob/
                   javac Pavan.java
                   java Pavan
                   echo 'built!' 
                """
            }
        }
        stage('Stage 3') {
            steps {
                echo 'tested!' 
            }
        }
        stage('Stage 5') {
            steps {
                echo 'deployed!' 
            }
        }
    }
}
