properties([pipelineTriggers([pollSCM('* * * * *')])])
node {
    stage("clone"){
    checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/amichaizelig/Jenkins-test.git']]])    
    }
    stage("show files"){
        bat "dir"
        bat "print-hellow.py"
    }
}
