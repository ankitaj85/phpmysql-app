node{

    stage('SCM Checkout')
    {
        git url: 'https://github.com/ankitaj85/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
    stage('PUSH image to Docker Hub')
    { 
        sh 'docker login -u doctorai -p Doctorai@123'
        sh 'docker push doctorai/phpmysql_app'
    }
}
