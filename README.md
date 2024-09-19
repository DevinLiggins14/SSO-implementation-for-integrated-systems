# SSO-implementation-for-integrated-systems
<h2>Description</h2>

<p align="center">
<img src="https://github.com/user-attachments/assets/fd782ffc-d154-4bbc-91e5-332e6711e9c1"/>

<h2>Languages and Utilities Used</h2>



<h2>Environments Used </h2>

- <b>CentOS Linux release 8.5.2111
 10</b>

<h2>Project walk-through:</h2>
<p align="center">
  <br/> To begin we need to make sure that the latest Java is installed on our system <br/>
<img src="https://github.com/user-attachments/assets/80ee5d6f-3564-483a-9e69-11445ae7d9aa"/>
  <br/> Now go to https://www.keycloak.org/downloads to download the tarball in our desired directory<br/>
 <img src="https://github.com/user-attachments/assets/6c5cff74-b583-4685-b75a-771b07c76d90"/>
  <img src="https://github.com/user-attachments/assets/2a27fa87-9b18-4d4e-9ba1-005d32456c32"/>
  <br/> Now confirm and extract the tarball in desired directory <br/> 
  <img src="https://github.com/user-attachments/assets/62dcdd7e-08d2-45f4-8827-2261a5d98eaa"/>
<br /> Before beginning installation let's set admin credentials <br/>
 <img src="https://github.com/user-attachments/assets/828a285f-2f91-4a0b-992f-671801363300"/>
 <br /> 
 <br/> Next lets start Keycloak in dev mode in the background. This is for testing purposes only and not advised for production use  <br/>
 <img src="https://github.com/user-attachments/assets/ba19d18c-4a43-4f5f-9acc-f2c22df86b2b"/>

<br/> Another way to run Keycloak is by using docker:  <br/>
<br/> First install docker on CentOS <br/>
<img src="https://github.com/user-attachments/assets/9f4b89a3-2449-405b-8c56-4cb5fb43f7ab"/>
<br/> Next navigate to https://www.keycloak.org/getting-started/getting-started-docker <br/>
<img src="https://github.com/user-attachments/assets/0d22828e-e8e5-4dcb-b528-385a69a016a1"/>
<br/> Next run the command found on the webpage locally on your machine <br/>
<img src="https://github.com/user-attachments/assets/70f2d1e3-8850-4d91-a574-1ff054d95508"/>
<br/> Make sure that port 8080 is not in use run netstat -tunlp | grep 8080 to confirm <br/>
<img src="https://github.com/user-attachments/assets/ff336780-f4a6-4033-b85d-708144d39a28"/>
<br/> Kill the java process we start ealier to follow the keycloak container method <br/>
<img src="https://github.com/user-attachments/assets/856ea7da-4892-4295-ba49-5c7676225cb2"/>
<br/> Add the -d parameter to run the keycloak image in detached mode and confirm its running <br/>
<img src="https://github.com/user-attachments/assets/dfd6739b-ff04-48fa-849a-4c5bd287b3a3"/>
<br/> In the web brower search ip addr or hostname :8080/admin and login with credentials from earlier  <br/>
<img src="https://github.com/user-attachments/assets/7bb44c5c-c7c4-4faf-b7c3-376a398984c0"/>
<img src="https://github.com/user-attachments/assets/aa64c4c5-0b27-4614-83a7-69c2f4f4fb0b"/>
 <br />  
 
<br />
  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />  <br/>
<img src=""/>
 <img src=""/>
<br />  <br/>
 <img src=""/>
 <br /> 
 <br/>  <br/>
 <img src=""/>
 <br />  
<br />
