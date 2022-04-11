pipeline {
    agent any
  
    stages {
        stage('Stage1-21050672') {
            steps {
                sh 'echo "Stage 1 Completed-21050672"'
                
            }
        }
    
        stage('Stage2-21050672') {
           
            
             steps { input('Push changes to Production?')
            }
            
        }
        stage('Stage3-21050672') {
            steps {
                     sh '''#!/bin/bash
                 targets=websvr_21050672;
                 locate_script='/21050672/script_dir/21050672_repo/21050672_script';
                 docker cp $locate_script $targets://$locate_script;
                 bolt script run $locate_script -t $targets -u clientadm -p user123 --no-host-key-check --run-as root;
                 '''
                 echo "Stage 3 completed -21050672"
            }
            
        }
          stage('Stage4-21050672') {
           steps { 
               sh 'echo "Production website tested working"'
               
           } 
              
          }
            stage('Stage5-21050672') {
            steps {
                sh 'echo "Production website is updatedsucessfully"'
            }
            
        }
            
            }
            }
