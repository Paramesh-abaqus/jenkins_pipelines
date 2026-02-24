pipeline {
    agent any

  /*  stages{
        stage("build_stage_1"){
            agent {label "slave1"}
            steps{
                sh "echo 'build_stage_1'"
                sh ''' sleep 10'''
            }
        }

        stage("buil_stage2"){
            agent {label "slave2"}
            steps{
                sh "echo 'build_stage_2'"
                 sh ''' ls -lrt
                pwd
                env

                sleep 10
                '''
            }
        }
    } */


    stages{
        stage("git_checkout"){
          //  agent {label "slave1"}
            steps{
                git branch: 'main', credentialsId: 'param-github', url: 'https://github.com/Paramesh-abaqus/jenkins_pipelines.git'
            }
        }

         stage("git_list files"){
          //  agent {label "slave1"}
            steps{
                sh ''' ls -lrt
                pwd
               sleep 10
                '''
            }
        }

          stage("git_build files"){
          //  agent {label "slave1"}
            steps{
                sh ''' ls -lrt
                pwd
               sleep 10
                '''
            }
        }

        stage("checkout test"){
         //   agent {label "slave2"}
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'param-github', url: 'https://github.com/Paramesh-abaqus/spring-6-webapp.git']])
            }
        }

        stage("checkout_list files"){
         ///   agent {label "slave2"}
            steps{
                sh ''' ls -lrt
                pwd
               sleep 10
                '''
            }
        }

          stage("checkout_build files"){
          //  agent {label "slave2"}
            steps{
                sh ''' ls -lrt
                pwd
               sleep 10
                '''
            }
        }
    }
}


