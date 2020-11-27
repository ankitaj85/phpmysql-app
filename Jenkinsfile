node{

    stage('SCM Checkout')
    {
        git credentialsId: '4cc785e9-441d-4818-a248-2bfb2148004d', url: 'https://github.com/VardhanNS/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'export DOCKER_HOST=127.0.0.1:2375'
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
    stage('PUSH image to Docker Hub')
    {
        sh 'docker login -u "doctorai" -p "Doctorai@123" docker.io'
        
        sh 'docker push doctorai/edurekajob1_web'
    }
}
