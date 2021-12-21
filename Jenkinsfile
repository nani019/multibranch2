node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
stage('continuous deploy')
{
sh 'scp /home/ubuntu/.jenkins/workspace/development/webapp/target/webapp.war ubuntu@172.31.31.73:/var/lib/tomcat8/webapps/qaenv4.war'
}
stage('continuous testing')
{
sh 'echo "test passed"'
}
stage('continuous delivery')
{
sh 'scp /home/ubuntu/.jenkins/workspace/development/webapp/target/webapp.war ubuntu@172.31.23.64:/var/lib/tomcat8/webapps/prodenv4.war'
}
}
