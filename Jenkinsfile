node {

    stage ('checkout'){

    git  'https://github.com/nitinrocksss/JenkinsTest3.git'

        }
    stage('mvn package'){

    def maven_home= tool name: 'MAVEN_HOME', type: 'maven'
    def mvn_cmd = "${maven_home}/bin/mvn"
    " bat ${mvn_cmd} mvn clean package"
    }
    
     stage('SonarQube Analysis') {
        def maven_home= tool name: 'MAVEN_HOME', type: 'maven'
        withSonarQubeEnv('sonar-7.5') { 
           " bat ${mvnHome}/bin/mvn sonar:sonar"
}
}
}
