pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     stepsv {
        //         checkout ([$class: 'GitSCM',
        //         branches: [[name: '*/main']],
        //         userRemoteConfigs: [[url: 'https://github.com/Burugupalli-Yogitha/PES2UG21CS126_Jenkins.git']]])
        
        //     }
        // }
        stage('Build') {
            steps {
                build 'PES2UG21CS126-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage( 'Test') {
            steps {
                sh './output'
            }
        }
        stage( 'Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
