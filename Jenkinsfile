pipeline {
   environment {
    front = "javier322/sentiment-analysis-frontend:$BUILD_NUMBER"
    frontUrl= " sa-frontend/."
    registryCredential = 'dockerhub'
    dockerImage = ''
  }
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/javier322/k8s-mastery.git'
      }
    }
     stage('Building image') {
      steps{
        script {
          dockerImage1=docker.build(front, frontUrl)
    
        }
      }
    }
    stage('Deploy Image') {
      steps{
        script {
          docker.withRegistry( '', registryCredential ) {
            dockerImage1.push()
          }
        }
      }
    }
    stage('Remove Unused docker image') {
      steps{
        sh "docker rmi $front"
      }
    }
     stage('Apply Kubernetes files'){
            steps{
            withKubeConfig([credentialsId: 'cluster', serverUrl:'https://a807fbb4-14ff-4f72-a1cf-f1c85a3717b2.k8s.ondigitalocean.com']){
             sh 'kubectl --namespace kube-system get pods'
             sh 'cat resource-manifests/sa-frontend-deployment-lb.yaml | sed "s/{{BUILD_NUMBER}}/$BUILD_NUMBER/g"  | kubectl apply -f - '
             sh 'kubectl apply -f resource-manifests/service-sa-frontend.yaml'
            }
        }
    }
  }
}
    


