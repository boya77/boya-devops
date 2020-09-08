pipeline {
    agent {
        label "slave-jenkins"
    }

    stages {
        stage('Hello') {
            steps {
                echo "hello world"
            }
        }
        stage('gitcheckout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/boya77/boya-devops.git']]])
            }            
        }
        stage(pwd) {
            steps {
               sh 'pwd'
	       sh 'cat /proc/cpuinfo'
            }
        }
    }   
}
