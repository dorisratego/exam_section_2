node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t exam_section_2:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'dratego' -p 'Letitbe123\$' "
sh "docker tag exam_section_2:latest dratego/exam_section_2:latest"
sh "docker push dratego/exam_section_2:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}
  
  stage('Run'){
  sh "docker run -d -p 3259:80/tcp exam_section_2:latest"}


}
