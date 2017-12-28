#!groovy
pipeline {
    agent {label 'master'}
environment 
{
        
imagename = 'adilashraf_10615395_img'
        
containername = 'adilashraf_10615395_con'
        
storagepath = "example-repo-local/adilashraf_10615395"      
buildnumber  = "${currentBuild.number}"
    
}
    stages {
            


stage('docker stop app1'){

agent{ label 'master' }

steps{
sh 'docker rm -f app1'
}

}

stage('docker start app1'){

agent{ label 'master' }

steps{
sh 'docker run -it  -d --name app1 malu/tomcat'
}

                   
}

stage('docker stop app2'){

agent{ label 'master' }

steps{
sh 'docker rm -f app2'
}

}

stage('docker start app2'){

agent{ label 'master' }

steps{
sh 'docker run -it  -d --name app2 malu/tomcat'
}


}


}
}
