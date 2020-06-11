node{
stage('SCM Checkout'){
git'https://github.com/mamatha-eng/testing'
}
/*stage('Compile-package'){
def mvnhome= tool name: 'maven-3', type: 'maven'
bat "${mvnHome}/bin/mvn package" 
}
}*/
stage('Compile-package'){
def mvn_version = 'maven-3'
withEnv( ["PATH+MAVEN_HOME=${tool mvn_version}/bin"] ) {
  bat "mvn -Dmaven.test.failure.ignore=true clean package"
 }
}
}
