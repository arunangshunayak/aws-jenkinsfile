properties([parameters([choice(choices: ['start', 'stop'], 
                            description: 'Select a choice to take action', name: 'choice'),
                        string(defaultValue: '', 
                               description: 'Add your Instance Id here', name: 'instanceId', trim: false)])])                
    node {
        
      if ( "${choice}" == "start" ){
              stage("Start Instance ") {
                                            
                sh "aws ec2 start-instances --instance-ids ${instanceId}"
                
                }
            }
            
            if ( "${choice}" == "stop" ){
            stage("Stop Instance ") {
                        
                sh "aws ec2 stop-instances --instance-ids ${instanceId}"
                }
            
            }
    }
