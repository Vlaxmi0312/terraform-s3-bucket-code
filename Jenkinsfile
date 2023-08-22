pipeline {
    agent any

        stages {
          stage('Checkout') { 
          steps { 
          checkout([$class: 'GitSCM', branches: [[name: "/master']], extensions: [], userRemoteConfigs: [[url: 'https://https://github.com/Vlaxmi0312/terraform-s3-bucket-code.git']]])
      }
  }
        stage ("terraform init") { 
          steps { 
            sh ('terraform init')
      }
  }
        stage ("terraform Action") {
         steps {
           echo "Terraform action is --> ${action}"
           sh ('terraform $(action)--auto-approve')
      }
    }
  }
}
