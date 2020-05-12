node{

def tomcatWeb = 'D:\\Apache\\apache-tomcat-8.0.35\\webapps'
def tomcatBin = 'D:\\Apache\\apache-tomcat-8.0.35\\bin'
def tomcatStatus = ''

stage('Scm Checkout'){

git 'https://github.com/Tdgopal/java-hello-world-webapp.git'
}
stage('Compile pkg create war file'){

def mvnHome = tool name: 'maven-3', type: 'maven'
bat "${mvnHome}/bin/mvn package"
}
 stage('Deploy to Tomcat'){
bat "copy target\\maven-helloworld.war \"${tomcatWeb}\\maven-helloworld.war\""
}
stage('Start Tomacat Server'){
bat "${tomcatBin}\\startup.bat"
} 
}
