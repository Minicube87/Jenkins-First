pipeline { 
  agent any 
 
  stages { 
    stage('Build') { 
      steps { 
        sh 'echo "Starte Build-Prozess..."' 
      } 
    } 
 
    stage('Test') { 
      steps { 
        sh ''' 
          echo "Führe Tests aus..." 
          ls -l 
        ''' 
      } 
    } 
 
    stage('Deploy') { 
      steps { 
        sh 'echo "Simuliere Deployment..."; sleep 1; echo "Deployment abgeschlossen!"' 
      } 
    } 
 
    stage('Cleanup Workspace') { 
      steps { 
        sh 'rm -rf ./* || true' 
      } 
    } 
  } 
 
  post { 
    always { 
      echo 'Pipeline abgeschlossen (always).' 
    } 
    success { 
      echo 'Alles grün (success).' 
    } 
    failure { 
      echo 'Da ist was schiefgelaufen (failure).' 
    } 
  } 
} 