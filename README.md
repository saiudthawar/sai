# sai
"sudo find /root -name credentials -ls",
				"echo done"





script for reboot and linux 

{
   "schemaVersion":"2.0",
   "description":"Run a script",
   "parameters":{
      "commands":{
         "type":"StringList",
         "description":"(Required) Specify a shell script or a command to run.",
         "minItems":1,
         "displayType":"textarea"
      }
   },
   "mainSteps":[
      {
         "action":"aws:runShellScript",
         "name":"runShellScript",
         "inputs":{
            "runCommand":[
                "sudo yum update -y",
                "sleep 10; reboot &",
                 "exit 0" ]
            }
        }
      
  ]
}
