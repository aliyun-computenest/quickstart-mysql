<h1>MySQL Community Edition Service Instance Deployment Document </h1>

<h2> Overview </h2>

<p>MySQL is a small, open source relational database management system. MySQL provides community edition services on the computing nest. You can quickly deploy MySQL services and implement O & M monitoring on the computing nest without configuring the cloud host, so you can easily build your own applications based on MySQL. This article describes how to activate the MySQL Community Edition service on the computing nest, as well as the deployment process and usage instructions. </p>

<h2> Billing instructions </h2>

<p> The cost of MySQL Community Edition on computing nest mainly involves:</p>

<ul>
<li> Selected vCPU and Memory Specifications </li>
<li> System disk type and capacity </li>
<li> Internet bandwidth </li>
<li> Database configuration </li>
</ul>

<p> Billing methods include:</p>

<ul>
<li> Pay-As-You-Go (hourly)</li>
<li> monthly package </li>
</ul>

<p> The estimated cost is visible in real time when the instance is created. </p>

<h2> Deployment Architecture </h2>

<p>MySQL Community Edition uses a stand-alone deployment architecture. </p>

<h2> Permissions required for RAM accounts </h2>

<p> The MySQL service needs to access and create resources such as ECS and VPC. If you use a RAM user to create a service instance, you need to add the corresponding resource permissions to the account of the RAM user before creating the service instance. For more information about how to add RAM permissions, see <a href = "https://help.aliyun.com/document_detail/121945.html"> Authorize RAM users </a>.
. The required permissions are shown in the following table. </p>

<table>
<thead>
<tr>
<th> Permission policy name </th>
<th> Remarks </th>
</tr>
</thead>
<tbody>
<tr>
<td>AliyunECSFullAccess</td>
<td> Permissions to manage ECS </td>
</tr>
<tr>
<td>AliyunVPCFullAccess</td>
<td> Permissions for managing VPC networks </td>
</tr>
<tr>
<td>AliyunROSFullAccess</td>
<td> Manage permissions for Resource Orchestration Services (ROS) </td>
</tr>
<tr>
<td>AliyunComputeNestUserFullAccess</td>
<td> Manage user-side permissions for the compute nest service (ComputeNest) </td>
</tr>
<tr>
<td>AliyunCloudMonitorFullAccess</td>
<td> Permissions to manage CloudMonitor (CloudMonitor) </td>
</tr>
</tbody>
</table>

<h2> Deployment process </h2>

<h3> Deployment steps </h3>

<p> Click <a href = "https://computenest.console.aliyun.com/user/cn-hangzhou/serviceInstanceCreate?ServiceId=service-2cf2013cb5084c318628"> Deploy Link </a>
, enter the service instance deployment interface, according to the interface prompt, fill in the parameters to complete the deployment. </p>

<h3> Deployment parameters </h3>

<p> When you create a service instance, you need to configure the service instance information. The following section describes the input parameters of the MySQL Community Edition service instance. </p>

<table>
<thead>
<tr>
<th> Parameter group </th>
<th> Parameter item </th>
<th> Example </th>
<th> Description </th>
</tr>
</thead>
<tbody>
<tr>
<td> Service instance name </td>
<td></td>
<td>test</td>
<td> Name of the instance </td>
</tr>
<tr>
<td> Region </td>
<td></td>
<td> China (Hangzhou)</td>
<td> Select the region of the service instance. We recommend that you select the region nearby to obtain better network latency. </td>
</tr>
<tr>
<td> Availability Zone Configuration </td>
<td> Deployment area </td>
<td> Availability Zone I</td>
<td> Different available regions in the region </td>
</tr>
<tr>
<td> Payment type configuration </td>
<td> Payment type </td>
<td> Pay-As-You-Go or Subscription </td>
</tr>
<tr>
<td> Select an existing basic resource configuration </td>
<td>VPC ID</td>
<td>vpc-xxx</td>
<td> Select the ID of the VPC. </td>
</tr>
<tr>
<td> Select an existing basic resource configuration </td>
<td> Switch ID</td>
<td>vsw-xxx</td>
<td> Select the switch ID. If the switch cannot be found, try switching the region and zone. </td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> Instance type </td>
<td>ecs.g7.large</td>
<td> Instance type, which can be selected according to actual needs </td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> System disk type </td>
<td>ESSD </td>
<td> System disk type, which can be selected according to actual needs </td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> System disk space </td>
<td>40</td>
<td> System disk space can be selected according to actual needs </td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> Data disk type </td>
<td>ESSD </td>
<td> Data disk type, which can be selected according to actual needs </td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> Data disk space </td>
<td>40</td>
<td> Data disk space, which can be selected according to actual needs </td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> Instance password </td>
<td><strong><em>*</strong></em>*</td>
<td> Set the instance password. 8 to 30 characters in length and must contain three items (uppercase letters, lowercase letters, numbers, and special symbols in)</td>
</tr>
<tr>
<td>ECS instance configuration </td>
<td> Enable public IP</td>
<td>true</td>
<td> Whether to enable public IP</td>
</tr>
<tr>
<td> Database configuration </td>
<td>root account password </td>
<td><strong><em>*</strong></em>*</td>
<td> Database root account password, length 8-32 characters, can contain large and small letters, numbers and special symbols </td>
</tr>
</tbody>
</table>

<p><img src="1.jpg" alt="1.jpg" /></p>

<h3> Verify Results </h3>

<ol>
<li> View the service instance.
After the service instance is created successfully, the deployment time takes about 2 minutes. After the deployment is complete, the corresponding service instance is displayed on the page. </li>
</ol>

<p><img src="2.jpg" alt="2.jpg" /></p>

<ol start="2">
<li> Access MySQL through a service instance </li>
</ol>

<p><img src="3.jpg" alt="3.jpg" />
After entering the corresponding service instance, you can get the DBConnectionPrivateAddress on the page. </p>

<h3> Using MySQL</h3>

<p> Please visit the MySQL website to learn how to use MySQL:<a href = "https://dev.mysql.com/doc/">MySQL Usage Documentation </a></p>
