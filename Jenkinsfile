pipeline {
    agent any
    tools { 
        maven 'Maven 3.6.3' 
        jdk 'jdk11' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    echo "M2_HOME = ${JAVA_HOME}"
                ''' 
            }
        }
        stage("java_pipeline_proj - Build") {
            steps {
            sh 'mvn install'
            }
        }
        stage("docker image build") {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    echo "M2_HOME = ${JAVA_HOME}"
                ''' 
            }
        }
        stage("deploy") {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    echo "M2_HOME = ${JAVA_HOME}"
                ''' 
            }
        }
    }
}
