*********************************************************************************************************
Task 1, Job 1

Problem: When developer commit code then jenkins fetch it and build it then deploy on docker(dev-docker) constainer

Solution:

1.	Get public ip address for jenkins by using ngrok
2.	Create a webhook on gitHub
3.	Run docker on dev-docker system and also enable remote(tcp) execution of docker command from jenkins(make sure jenkins user added in docker group)
4.	Add docker in cloud node on jenkins
5.	Create job **(step 6-12)** :
6.	Take code from github
7.  Use webhook trigger
8.  Restrict job on docker server
9.	Define which image to be used for launching docker container
10.	Add maven command to be executed
11.	Deoloy package on docker container
12.	Also enable artifact

Lets start with setup

1. Get public ip address for jenkins by using ngrok
![image](https://user-images.githubusercontent.com/75135128/122684343-86f73100-d222-11eb-9252-11c40b2f4cf2.png)

2. Create a webhook on gitHub
![image](https://user-images.githubusercontent.com/75135128/122684523-6c718780-d223-11eb-9b01-b929d73556fc.png)

3. Run docker on dev-docker system and also enable remote(tcp) execution of docker command from jenkins
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

9. Define which image to be used for launching docker container(Image name defined in step 4)
10. Add maven command to build and package the application
![image](https://user-images.githubusercontent.com/75135128/122684910-f4f12780-d225-11eb-9d86-bda11afa81a7.png)

11.	Deoloy package on docker container
![image](https://user-images.githubusercontent.com/75135128/122684932-1baf5e00-d226-11eb-9c99-a6f2144ec7a0.png)

12.	Enable artifact
![image](https://user-images.githubusercontent.com/75135128/122684940-2d910100-d226-11eb-914f-74492ac45677.png)


Whenever any developer commit any change then jenkins start build
![image](https://user-images.githubusercontent.com/75135128/122685323-34b90e80-d228-11eb-8006-ef160e033063.png)

4th Build triggered

![image](https://user-images.githubusercontent.com/75135128/122685328-413d6700-d228-11eb-8c84-15dfb013744b.png)

New container launched

![image](https://user-images.githubusercontent.com/75135128/122685342-574b2780-d228-11eb-844c-63af79280e46.png)

Console output that shows user who trigger this build (here is github) and the system on which job is building is in progress 

![image](https://user-images.githubusercontent.com/75135128/122685375-8feb0100-d228-11eb-9e17-0e0b8a05e8e5.png)

Final output of the build

![image](https://user-images.githubusercontent.com/75135128/122685468-29b2ae00-d229-11eb-8b61-97de124c840e.png)

After completion of job docker container automatically stopped

Using this setup you can dynamically launch conatiners and deploy your app on the top of these containers.

*********************************************************************************************************

Task 1, Job 2

Problem: When developer commit and push the code then jenkins fetch it and build it, test it and package and deploy on docker(master-docker) constainer
Solution:

1.	Get public ip address for jenkins by using ngrok
2.	Create a webhook on gitHub
3.	Run docker on master-docker system and also enable remote(tcp) execution of docker command from jenkins(make sure jenkins user added in docker group)
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
![image](https://user-images.githubusercontent.com/75135128/122815579-44515980-d2f3-11eb-9e51-569c54be02f1.png)

2. Create a webhook on gitHub
![image](https://user-images.githubusercontent.com/75135128/122817424-8085b980-d2f5-11eb-8f14-691e7e575285.png)

3. Run docker on other system and also enable remote(tcp) execution of docker commad on docker server
![image](https://user-images.githubusercontent.com/75135128/122820550-5e8e3600-d2f9-11eb-89a4-1c570f73c8eb.png)

4. Add docker in cloud node on jenkins
![image](https://user-images.githubusercontent.com/75135128/122817483-95624d00-d2f5-11eb-9f43-1b6515b2af24.png)

5. Create job (step 6-12):
6. Take code from github
![image](https://user-images.githubusercontent.com/75135128/122817909-29341900-d2f6-11eb-870d-c4e7412e413e.png)

7.  Use webhook trigger
![image](https://user-images.githubusercontent.com/75135128/122817878-1c172a00-d2f6-11eb-8289-e41fa6e942b3.png)

8. Restrict job on docker server
![image](https://user-images.githubusercontent.com/75135128/122817764-f722b700-d2f5-11eb-80f1-ee838c9259d6.png)

9. Define which image to be used for launching docker container(Image name defined in step 4)
10. Add maven command to build and pack the application
![image](https://user-images.githubusercontent.com/75135128/122820911-ca709e80-d2f9-11eb-90ad-97861a287f0d.png)

11.	Deoloy package on docker container itself
![image](https://user-images.githubusercontent.com/75135128/122820948-d9575100-d2f9-11eb-9072-244188bfe376.png)

12.	Enable artifact
![image](https://user-images.githubusercontent.com/75135128/122820971-e07e5f00-d2f9-11eb-9b69-fdd14ba40990.png)


Whenever any developer commit any change then jenkins start build
![image](https://user-images.githubusercontent.com/75135128/122819264-d8252480-d2f7-11eb-8906-5098b933abc4.png)
4th Build triggered
![image](https://user-images.githubusercontent.com/75135128/122819313-ea06c780-d2f7-11eb-9923-75632775881d.png)

New container launched
![image](https://user-images.githubusercontent.com/75135128/122819383-0571d280-d2f8-11eb-8aa6-8d69eaae4f39.png)


Console output that shows user who trigger this build (here is github) and the system on which job is building is in progress 
![image](https://user-images.githubusercontent.com/75135128/122819545-3c47e880-d2f8-11eb-9325-60325777d6aa.png)


Final output of the build:  

Compile
![image](https://user-images.githubusercontent.com/75135128/122819975-bb3d2100-d2f8-11eb-8f1d-05588dd92286.png)

Test
![image](https://user-images.githubusercontent.com/75135128/122819754-7913df80-d2f8-11eb-9ea0-14aa2f69ecb4.png)

Packaging done
![image](https://user-images.githubusercontent.com/75135128/122820081-d871ef80-d2f8-11eb-8b8b-5df59412c0d2.png)

Deployed on Master-Docker
![image](https://user-images.githubusercontent.com/75135128/122820154-eb84bf80-d2f8-11eb-98e8-160f932d8f6f.png)

Build completed with Artifacts
![image](https://user-images.githubusercontent.com/75135128/122820366-25ee5c80-d2f9-11eb-9a9a-0edec0c1e2bc.png)

After completion of job docker container automatically stopped.

Using this setup you can dynamically launch conatiners and deploy your app on the top of these containers.


*********************************************************************************************************
