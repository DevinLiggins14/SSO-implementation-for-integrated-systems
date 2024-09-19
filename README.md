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
 Click on keycloak on the left and select create realm to create a new realm
<br />
<img src="https://github.com/user-attachments/assets/f1ff6b56-268c-4362-a77b-e34fd34e2cf7"/>
<br/>  Configure when done <br/>
<img src="https://github.com/user-attachments/assets/9e0edd5a-614c-4fbe-89df-acd1ae1e3e2c"/>
  <br/>
  <br/> CLick create <br/>
<img src="https://github.com/user-attachments/assets/b31ce90a-5be4-445d-951d-0d6ab50b9194"/>
 <img src="https://github.com/user-attachments/assets/5e0a9573-c002-47b3-9316-162c18e77bd3"/>
<br /> Navigate to create client and pick OpenID and write portainer <br/>
 <img src="https://github.com/user-attachments/assets/1557919a-5105-4261-8309-fc1181a410b8"/>
 <br /> 
 <br/> On the next page select client authentication and service account roles on and leave rest as default  <br/>
 <img src="https://github.com/user-attachments/assets/88c1f257-5d48-4707-b693-d7c376cf5ce3"/>
 <br />  
<br /> Add desired links for application <br/>
<img src="https://github.com/user-attachments/assets/38528bba-5154-436a-a671-ebddb4c36be0"/>
<br/> Confirm creation when finished <br/>
 <img src="https://github.com/user-attachments/assets/daf1a1ef-f140-463b-bf99-f4e0e304551d"/>
 <br/> Confirm configurations for application <br/>
 <img src="https://github.com/user-attachments/assets/f0ab99a3-b5d6-4f1d-ab07-568b0f58fedc"/>
<br /> To confirm and test our SSO we require an application. We can use Grafana, first download the grafana image locally on your machine <br/>
 <img src="https://github.com/user-attachments/assets/bfb034cc-bc56-4a7b-bc76-85fa6545fe3e"/>
 <br /> 
 <br/> Confirm installation and access the Grafana UI <br/>
 <img src="https://github.com/user-attachments/assets/f933d7ab-0bd6-479b-8b16-e29608d19bfc"/>
 <img src="https://github.com/user-attachments/assets/ebd9a43a-b637-4cb9-b8f4-4cfe5ec42c5a"/>
 <img src="https://github.com/user-attachments/assets/8998f6c0-6e53-447e-a891-3094ea8a0420"/>
 <br />  
<br /> Now navigate to adminstration and authentication <br/>
<img src="https://github.com/user-attachments/assets/3fdcdf24-4c0e-4e39-84f4-d8d87a4e5fd9"/>
<br/> Select OpenAuth <br/>
 <img src="https://github.com/user-attachments/assets/f3918a4e-7438-47e3-bc53-dd3eddf3329c"/>
 <br/> Return to the keycloak and create a user for Grafana <br/>
 <img src="https://github.com/user-attachments/assets/c41f81aa-6f5d-4caf-93af-1b9e276a62de"/>
 <img src="https://github.com/user-attachments/assets/bdd4c645-cb34-4c4e-8732-f57b2a62e61b"/>
 <br/> Navigate to the newly created clients credentials page and copy the secret<br/>
 <img src="https://github.com/user-attachments/assets/58bc2993-b0b9-441f-9b14-d063e5cfa977"/>
 <br/>
<br /> Paste the Grafana secret in the UI back on the Grafana page  <br/>
 <img src="https://github.com/user-attachments/assets/9f0683b5-3364-461a-9414-d1944822b981"/>
 <br /> 
 <br/> Add the remaining keycloak url and token and confirm <br/>
 <img src="https://github.com/user-attachments/assets/a7148dbd-e61d-44e7-a991-44de33072582"/>
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
