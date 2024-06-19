pipeline {
    agent any
    
    environment {
        
        SCANNER_HOME = tool 'sonar-scanner'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'latest', url: 'https://github.com/amanpatelitofficial/10-Tier-MicroService-Appliction.git'
            }
        }
        
        stage('SonarQube') {
            steps {
                
                withSonarQubeEnv('sonar') {
                    sh ''' $SCANNER_HOME/bin/sonar-scanner -Dsonar.projectKey=10-Tier -Dsonar.projectName=10-Tier -Dsonar.java.binaries=. '''
                }
               
            }
        }
        
        stage('adservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/adservice/') {
                                 sh "docker build -t amanpatelitprofessional/adservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/adservice:latest"
								 sh " docker rmi amanpatelitprofessional/adservice:latest"
                        }
                    }
                }
            }
        }
		
		stage('cartservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/cartservice/src/') {
                                 sh "docker build -t amanpatelitprofessioanl/cartservice:latest ."
                                 sh "docker push amanpatelitprofessioan/cartservice:latest"
								 sh " docker rmi amanpatelitprofessioan/cartservice:latest"
                        }
                    }
                }
            }
        }
		
		stage('checkoutservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/checkoutservice/') {
                                 sh "docker build -t amanpatelitprofessioanl/checkoutservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/checkoutservice:latest"
								 sh " docker rmi amanpatelitprofessioanl/checkoutservice:latest"
                        }
                    }
                }
            }
        }
		
		stage('currencyservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/currencyservice/') {
                                 sh "docker build -t amanpatelitprofessioanl/currencyservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/currencyservice:latest"
								 sh " docker rmi amanpatelitprofessioanl/currencyservice:latest"
                        }
                    }
                }
            }
        }
        
		stage('emailservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/emailservice/') {
                                 sh "docker build -t amanpatelitprofessioanl/emailservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/emailservice:latest"
								 sh " docker rmi amanpatelitprofessioanl/emailservice:latest"
                        }
                    }
                }
            }
        }
		
		stage('frontend') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/frontend/') {
                                 sh "docker build -t amanpatelitprofessioanl/frontend:latest ."
                                 sh "docker push amanpatelitprofessioanl/frontend:latest"
								 sh " docker rmi amanpatelitprofessioanl/frontend:latest"
                        }
                    }
                }
            }
        }
		
		stage('loadgenerator') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/loadgenerator/') {
                                 sh "docker build -t amanpatelitprofessioanl/loadgenerator:latest ."
                                 sh "docker push amanpatelitprofessioanl/loadgenerator:latest"
								 sh " docker rmi amanpatelitprofessioanl/loadgenerator:latest"
                        }
                    }
                }
            }
        }
		
		stage('paymentservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/paymentservice/') {
                                 sh "docker build -t amanpatelitprofessioanl/paymentservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/paymentservice:latest"
								  sh " docker rmi amanpatelitprofessioanl/paymentservice:latest"
                        }
                    }
                }
            }
        }
        
		stage('productcatalogservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/productcatalogservice/') {
                                 sh "docker build -t amanpatelitprofessioanl/productcatalogservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/productcatalogservice:latest"
								 sh " docker rmi amanpatelitprofessioanl/productcatalogservice:latest"
                        }
                    }
                }
            }
        }
		
		stage('recommendationservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/recommendationservice/') {
                                 sh "docker build -t amanpatelitprofessioanl/recommendationservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/recommendationservice:latest"
								 sh " docker rmi amanpatelitprofessioanl/recommendationservice:latest"
                        }
                    }
                }
            }
        }
		
		stage('shippingservice') {
            steps {
                script{
                    withDockerRegistry(credentialsId: 'docker-cred', toolName: 'docker') {
                          dir('/var/lib/jenkins/workspace/10-Tier/src/shippingservice/') {
                                 sh "docker build -t amanpatelitprofessioan/shippingservice:latest ."
                                 sh "docker push amanpatelitprofessioanl/shippingservice:latest"
								 sh " docker rmi amanpatelitprofessioanl/shippingservice:latest"
                        }
                    }
                }
            }
        }
        
        
        	stage('K8-Deploy') {
            steps {
                withKubeConfig(caCertificate: '', clusterName: 'my-eks8', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', restrictKubeConfigAccess: false, serverUrl: 'https://2BCD568E04EC6456125F85067AFE81B9.gr7.ap-south-1.eks.amazonaws.com') {
                         sh 'kubectl apply -f deployment-service.yml'
                         sh 'kubectl get pods '
                         sh 'kubectl get svc'
                }
            }
        }
        
    }
}
