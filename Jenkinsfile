node{

def tomcatWeb = 'D:\\Apache\\apache-tomcat-8.0.35\\webapps'
def tomcatBin = 'D:\\Apache\\apache-tomcat-8.0.35\\bin'
def tomcatStatus = ''

stage('Scm Checkout'){

git 'https://github.com/Tdgopal/java-hello-world-webapp.git'
}
stage('Compile pkg create war file'){

def mvnHome = tool name: 'maven-default', type: 'maven'

bat "D://apache-maven-3.6.3/bin/mvn package"
}
stage('Deploy to Tomcat'){

bat "copy target\\jenkinswar.war 'D://Apache/apache-tomcat-8.0.35/webapps/jenkinswar.war/'
}
stage('Start Tomacat Server'){
sleep(time : 5, unit : "second" )
bat "D:\\Apache\\apache-tomcat-8.0.35\\bin\\startup.bat"
sleep(time : 100, unit : "second" )
}
