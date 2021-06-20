Task 1
Job1: When developer commit code then jenkins fetch it and build it then deploy on docker(running on remote system) constainer
1.	Get public ip address for jenkins by using ngrok
2.	Create a webhook on gitHub
3.	Run docker on other system
4.	Enable remote(tcp) execution of docker commad on docker server
5.	Add docker in cloud node on jenkins
6.	Create job: 
  a.	Take code from github
  b.	Use webhook trigger
  c.	Restrict job on docker server
  d.	Define which image to be used for launching docker container
  e.	Add maven command to be executed  
  f.	Deoloy package on docker container itself
  g.	Also enable artifact 
