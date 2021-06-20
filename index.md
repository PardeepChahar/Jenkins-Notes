Task 1
Job1: When developer commit code then jenkins fetch it and build it then deploy on docker(running on remote system) constainer
1.	Get public ip address for jenkins by using ngrok
2.	Create a webhook on gitHub
3.	Run docker on other system and also enable remote(tcp) execution of docker commad on docker server
4.	Add docker in cloud node on jenkins
5.	Create job **(step 6-12)** :
6.	Take code from github
7.  Use webhook trigger
8.  Restrict job on docker server																
9.	Define which image to be used for launching docker container																
10.	Add maven command to be executed																
11.	Deoloy package on docker container itself																
12.	Also enable artifact 																

Lets start with setup

1. Get public ip address for jenkins by using ngrok
![image](https://user-images.githubusercontent.com/75135128/122684343-86f73100-d222-11eb-9252-11c40b2f4cf2.png)

2. Create a webhook on gitHub
![image](https://user-images.githubusercontent.com/75135128/122684523-6c718780-d223-11eb-9b01-b929d73556fc.png)

3. Run docker on other system and also enable remote(tcp) execution of docker commad on docker server
![image](https://user-images.githubusercontent.com/75135128/122684688-8069b900-d224-11eb-8e52-a6caa885966b.png)

4. Add docker in cloud node on jenkins
![image](https://user-images.githubusercontent.com/75135128/122684754-0128b500-d225-11eb-928c-e85357c01334.png)

5. Create job (step 6-12):
6. Take code from github
![image](https://user-images.githubusercontent.com/75135128/122684809-611f5b80-d225-11eb-9ca8-3d6ca5a6ae62.png)

7.  Use webhook trigger
![image](https://user-images.githubusercontent.com/75135128/122684837-8d3adc80-d225-11eb-9880-4da7f025c520.png)

8. Restrict job on docker server
![image](https://user-images.githubusercontent.com/75135128/122684849-9deb5280-d225-11eb-94be-cdb390db8e8b.png)

9. Define which image to be used for launching docker container(See image name given in step 4)
10. Add maven command to be executed
![image](https://user-images.githubusercontent.com/75135128/122684910-f4f12780-d225-11eb-9d86-bda11afa81a7.png)

11.	Deoloy package on docker container itself
![image](https://user-images.githubusercontent.com/75135128/122684932-1baf5e00-d226-11eb-9c99-a6f2144ec7a0.png)

12.	Also enable artifact
![image](https://user-images.githubusercontent.com/75135128/122684940-2d910100-d226-11eb-914f-74492ac45677.png)


Whenever any developer commit any change then jenkins start build
![image](https://user-images.githubusercontent.com/75135128/122685323-34b90e80-d228-11eb-8006-ef160e033063.png)

Build triggered

![image](https://user-images.githubusercontent.com/75135128/122685328-413d6700-d228-11eb-8c84-15dfb013744b.png)

New container launched

![image](https://user-images.githubusercontent.com/75135128/122685342-574b2780-d228-11eb-844c-63af79280e46.png)

Console output that shows user who trigger this build (here is github) and the system on which job is building 

![image](https://user-images.githubusercontent.com/75135128/122685375-8feb0100-d228-11eb-9e17-0e0b8a05e8e5.png)

Final output of the build

![image](https://user-images.githubusercontent.com/75135128/122685468-29b2ae00-d229-11eb-8b61-97de124c840e.png)
