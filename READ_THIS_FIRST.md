<table>
   <thead>
      <tr>
         <th colSpan="2">ACMEAnnuityEJBMDB.ear</th>
      </tr>
   </thead>
  <tbody>
    <tr>
      <td>Migration plan</td>
      <td>WebSphere Liberty</td>
    </tr>
    <tr>
      <td>Migration complexity</td>
      <td>moderate</td>
    </tr>
     <tr>
        <td colSpan="2"><b>Summary of work</b></td>
     </tr>
     <tr>
        <td>Total issues</td>
        <td>21</td>
     </tr>
     <tr>
        <td>Estimated effort (days)</td>
        <td>10.0</td>
     </tr>
     <tr>
        <td>External dependencies</td>
        <td>
          6
        </td>
     </tr>
  </tbody>
</table>


### Source code project
This source code Maven project generated by Transformation Advisor enables you to make changes to your application before migrating it to Liberty. The analysis document and report available in Transformation Advisor describe the changes necessary for a successful migration. If you are using Eclipse, the [IBM WebSphere Migration Toolkit](https://www.ibm.com/developerworks/library/mw-1701-was-migration/index.html) makes source code updates easier. The toolkit is available in the [Eclipse Marketplace](https://marketplace.eclipse.org/).
 
 ### How the bundle helps with modernization
 
  - Provides files that are necessary for containerization, accelerating the deployment to Liberty.
  
  - Allows you to make and test changes to your application in a container in your local environment.
- Provides the resources necessary to deploy your application using an operator.
  
  <table>
   <thead>
      <tr><th align="center" colSpan="2">Bundle contents</th></tr>
   </thead>
  <tbody>
    <tr><td colSpan="2"><b>Files for building a containerized image</b></td></tr>
    <tr><td>server.xml</td><td>Contains the Liberty server configuration for the application you are migrating. It configures application dependencies such as database connections and messaging. The server.xml may need some updates - for example, adding passwords that have been hidden by Transformation Advisor. For more details see <a href='https://www.ibm.com/support/knowledgecenter/SS5Q6W/migrationArtifacts/deployApps.html' target='_blank'>link</a>.</td></tr><tr><td>jvm.options</td><td>This is an optional file that will exist only if jvm options were configured in the source server. This file allows you to specify server startup options such as <b>-X</b> arguments.</td></tr><tr><td>pom.xml</td><td>The pom.xml contains information about the project and configuration details used by Maven to build the project.</td></tr><tr><td>Dockerfile</td><td>The multi-stage Dockerfile first builds the Maven project and then uses the build output to build a docker image which includes your application configured in Liberty.</td></tr>
    <tr>
       <td colSpan="2"><b>Files for deploying</b></td>
    </tr>
    <tr><td>Application CR</td><td>A custom resource (CR) configuration for your application. This resource will create an instance of your application from the Open Liberty Operator in OpenShift</td></tr><tr>
<td colSpan="2"><b>Source directory</b></td>
</tr><tr><td>src</td><td>Contains a mini application that can be used to test your build and deploy process. After testing, you can copy your application's source code and resources into the source directory tree to start building and deploying.</td></tr>
  </tbody>
</table>  
 
 ### Documentation & support
 For more information and instructions on how to use this software see the [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/SS5Q6W/welcome.html). 