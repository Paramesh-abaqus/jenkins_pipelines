pipeline {
    agent none

    stages{
        stage("build_stage_1"){
            agent {label "slave1"}
            steps{
                sh "echo 'build_stage_1'"
            }
        }

        stage("buil_stage2"){
            agent {label "slave2"}
            steps{
                sh "echo 'build_stage_2'"
                ''' sh ls -lrt
                pwd
                evn
            }
        }{}
    }
}