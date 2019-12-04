properties([parameters([string(defaultValue: 'start',description: '', name: 'confirmation', trim: false)])])
                       
    node {
            if ( "${confirmation}" == "start" ){
              stage("Start Instance ") {
                            
                sh "aws ec2 start-instances --instance-ids i-09d3e733b4d42bcf7"
                            
                }
              }
            if ( "${confirmation}" == "stop" ){
            stage("Stop Instance ") {
                              
                sh "aws ec2 stop-instances --instance-ids i-09d3e733b4d42bcf7"
                
                }
              }
           }
