Task 1
Job1: When developer commit code then jenkins fetch it and build it then deploy on docker(running on remote system) constainer
1.	Get public ip address for jenkins by using ngrok
2.	Create a webhook on gitHub
3.	Run docker on other system
4.	Enable remote(tcp) execution of docker commad on docker server
5.	Add docker in cloud node on jenkins
6.	Create job(step 7-13):
7.	Take code from github
8.	Use webhook trigger																
9.	Restrict job on docker server																
10.	Define which image to be used for launching docker container																
11.	Add maven command to be executed																
12.	Deoloy package on docker container itself																
13.	Also enable artifact 																
