pipeline {
  agent any
  stages {
    stage('Destroy Webstack') {
      steps {
        parallel(
          "Destroy Beanstalk": {
            build 'Webstack-Dev-Beanstalk-Destroy'
            
          },
          "Destroy CacheServers": {
            build 'Webstack-Dev-Varnish-Destroy'
            
          }
        )
      }
    }
  }
}