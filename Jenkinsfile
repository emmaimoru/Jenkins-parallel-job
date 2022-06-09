pipeline{
	agent any
	stages{
		stage('version-control'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'ad', url: 'https://github.com/emmaimoru/Jenkins-parallel-job.git']]])
			}
		}
		stage('parallel-job'){
			parallel{
				stage('sub-job1'){
					steps{
						echo 'action1'
					}
				}
				stage('sub-job2'){
					steps{
						echo 'action2'
					}
				}
<<<<<<< HEAD
                stage('sub-job3'){
                    steps{
                        echo 'action3'
                    }
                }
                stage('sub-job4'){
                    steps{
                        echo 'action4'
                    }
                }
=======
         stage('sub-job3'){
           steps{
             echo 'action3'
           }
        }
>>>>>>> 63de610ccaf5cff2c99d7a433341e410203a6dd6
			}
		}
		stage('codebuild'){
			steps{
				sh 'cat /etc/passwd'
			}
		}	
	}
}
