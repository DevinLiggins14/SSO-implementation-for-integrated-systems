# SSO-implementation-for-integrated-systems
<h2>Description</h2>
The purpose of this project is to configure and integrate SSO and MKA to applications using Keycloak and use Gafrana and Prometheus to record metrics and system performance 
<p align="center">
<img src="https://github.com/user-attachments/assets/fd782ffc-d154-4bbc-91e5-332e6711e9c1"/>

<h2>Languages and Utilities Used</h2>

Bash, Yaml

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
<br /> Sign out of Grafana and now the SSO option is availible <br/>
<img src="https://github.com/user-attachments/assets/3fbba20b-7a5d-4f68-80e1-101cd774995e"/>
 <img src="https://github.com/user-attachments/assets/b2e7b146-e99b-4bbd-b925-5b4fc38cbae2"/>
  <br/> Select for instant access: <br/>
 <img src="https://github.com/user-attachments/assets/bd1e668b-118b-462a-bde2-c62a49ea7b11"/>
<br /> Display name can also be changed and customized <br/>
 <img src="https://github.com/user-attachments/assets/ea327591-ff8c-49b6-9f7d-481ec3a2fdd0"/>
 <img src="https://github.com/user-attachments/assets/6e4c14f9-1f4d-4c32-8e21-5d93a0edf90c"/>
 <br /> 
 <br/> Navigate to the admin role and go to authentication to select things required during sign on <br/>
 <img src="https://github.com/user-attachments/assets/36474bf1-531f-4775-a5f0-dfb17b23a8aa"/>
<br/> Turn on to authenticate client externally <br/> 
<img src="https://github.com/user-attachments/assets/564f97ea-5602-4140-85d4-fec40f80d102"/>
 <br />  
<br /> Go to the flows section in authentication <br/>
<img src="https://github.com/user-attachments/assets/fa8638c3-2b31-42df-8b69-2f68ee2cbdb2"/>
<br/> view current flow  <br/>
 <img src="https://github.com/user-attachments/assets/91e14699-01ac-4305-ae45-0d28f8a3134d"/>
<br /> Require OPT <br/>
 <img src="https://github.com/user-attachments/assets/edc83507-19b4-469d-abc0-6ab9874dd181"/>
 <br /> Confirm it works <br/>
 <img src="https://github.com/user-attachments/assets/918a2cb2-33cb-41c7-884f-43ccb5bbe3c3"/>
 <br/> Now SSO is required. After selecting the option below the default user and password worked <br/>
 <img src="https://github.com/user-attachments/assets/1ea9f312-7da3-40c2-8968-6dc018c48954"/>
 <br />  
<br /> Configure custom user requirements <br/>
<img src="https://github.com/user-attachments/assets/68d390f7-75d3-4832-95ac-205ccbfd3e4e"/>
<br/>
<br /> Navigate to Clients and roles and create role for the grafana client  <br/>
 <img src="https://github.com/user-attachments/assets/980fc923-3b39-47ea-847a-3ced8da1b515"/>
 <br /> 
 <br/> Acess the application via mobile with the role  <br/>
 <img src="https://github.com/user-attachments/assets/0c1d5436-027e-4969-8bf5-4e502632bab0"/>
 <br/> MKA & OTO required working after being tested <br/>
 <img src="https://github.com/user-attachments/assets/76ee2062-6d31-4ef7-8025-e7df58105bb8"/>
 <br/> Email one time code success after being configured and tested <br/>
 <img src="https://github.com/user-attachments/assets/12ce37ec-56af-408e-9e8b-b4a9905706a9"/>
 <br/> Successful sign in after one time code <br/>
 <img src="https://github.com/user-attachments/assets/96d38559-b15c-4a9b-a2a8-55761b5d2561"/>
 <br/>
 <br />  
<br /> To set up system monitoring we will use Grafana with Prometheus but first we must set up Prometheus <br/>
<img src="https://github.com/user-attachments/assets/3a8189dd-4437-489d-b2d0-c9a0921075d7"/>
 <img src=""/>
<br /> http://ip or hostname :9090 to access the UI <br/>
 <img src="https://github.com/user-attachments/assets/4efe3bbf-3610-4068-9024-0bab74f86975"/>
 <br /> Click on status to view machine metrics<br/>
 <img src="https://github.com/user-attachments/assets/18dc88aa-fa8b-4162-8346-f54a57441e88"/>
 <br/> In the Grafana UI go to connections and type Prometheus <br/>
 <img src="https://github.com/user-attachments/assets/024dae9e-3efe-48b5-a1eb-4b92eea4afe9"/>
 <img src="https://github.com/user-attachments/assets/964bce2c-01f8-48e8-9fd2-4b58d259d102"/>
 <br />  
<br /> Select OpenAuth <br/>
<img src="https://github.com/user-attachments/assets/0155f1f7-6f3e-448e-853e-c25aa1e31180"/>
 <img src=""/>
<br /> Note if configured incorrectly the plugin wont work properly <br/>
 <img src="https://github.com/user-attachments/assets/8249e20f-2c41-4cd5-8ad9-4289e329996f"/>
 <br /> 
 <br/> Click save and test when correctly confirgured <br/>
 <img src="https://github.com/user-attachments/assets/a2db357e-b5c9-4961-b0a8-72e4e35d6628"/>
 <br /> Time to test to fix the issue.  <br/>
 <img src="https://github.com/user-attachments/assets/f6ed3eac-0250-420f-936c-4bdbd485e910"/>
 <img src="https://github.com/user-attachments/assets/94163ecf-8391-40f3-97a2-a1d9123dc663"/>
<br /> Confirm if the IP address on the Prometheus vm running the container is correct <br/>
<br/> We can try another way. Go to dashboard select import make sure the format is in JSON or else...<br/>
<img src="https://github.com/user-attachments/assets/060204a1-ca99-4272-ab4d-1be6688fed0f"/>
<br/> Now with JSON <br/>
<br/> Select name and import<br/>
 <img src="https://github.com/user-attachments/assets/3cd2dac3-3e3e-4431-baea-af6992402196"/>
<br />
 <br /> 
 <br/> Return to adding the API server for Prometheus.. after much troubleshooting: <br/>
 <img src="https://github.com/user-attachments/assets/02504abc-875b-434b-9f56-bef23aff5209"/>
 <br />  
<br/> These are two VMs on Prometheus currently for example <br/>
 <img src="https://github.com/user-attachments/assets/e3094900-b66c-413d-b1a3-d768afc61df4"/>
<br /> On our dashboard let's set the time for the past 24hrs to recieve recent data from the day and then pick a custom query <br/>
 <img src="https://github.com/user-attachments/assets/8183bc5c-ed1e-4364-a37d-67134dc1cfa1"/>
 <br /> 
 <br/> Next pick the style of chat desired <br/>
 <img src="https://github.com/user-attachments/assets/63937b2a-8533-4164-bc16-707444b3362a"/>
 <br />  
<br /> Click add visualization to continue customization of metrics dashboard <br/>
<img src="https://github.com/user-attachments/assets/ec22a232-2b11-43fc-8c0c-d3a95061a6cb"/>
<br/> When desired select save <br/>
 <img src="https://github.com/user-attachments/assets/511d88dd-ff01-487e-bbdc-eb5cfd661ef1"/>
<br /> Data can also be queryed in the explore tab <br/>
 <img src="https://github.com/user-attachments/assets/b2d42e7f-3667-469d-92dc-622dccf8ea1c"/>
 <br/> Success! <br/>
 <br/> Head to alerting and define a metric to recieve routine alerts on vm system status as well as a designated email <br/>
 <img src="https://github.com/user-attachments/assets/be7455cc-5b86-4392-8bb4-e76095efa792"/>
 <img src="https://github.com/user-attachments/assets/772427be-a1c7-4b0e-9aa8-33bf81511f8f"/>
