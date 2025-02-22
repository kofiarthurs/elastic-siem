<h1>Elastic SIEM</h1>
<h2>Description</h2>
In today’s lab, We will set up ELK to monitor our Kali machine for nmap scans and send email alerts.

<h2>Deployment Option</h2>
<img src="https://imgur.com/2SoP4NU.png" height="80%" width="80%"/>

On signing up, select Elastic for Observability. I named my project MySiemLAB.

<img src="https://imgur.com/ccCEb9O.png" height="80%" width="80%"/>

Opening the deployment leads to the dashboard where we will be doing the next steps below.

<h2>Integrations</h2>
<img src="https://imgur.com/PUBy55Z.png" height="80%" width="80%"/>

Once everything was configured, select Integrations under Management and chose Elastic Defend.

<img src="https://imgur.com/JUk0oq2.png" height="80%" width="80%"/>


Click on Install Elastic Agent. The image below shows the installation options.

<img src="https://imgur.com/S9gDdU8.png" height="80%" width="80%"/>

I selected Linux Tar for my Kali Machine. Once installed, you will get a confirmation under Confirm Agent Enrollment.

<img src="https://imgur.com/EeE8OlH.png" height="80%" width="80%"/>

Under Fleet, we can see my Kali machine.

<h2>Discover & Dashboards</h2>
<img src="https://imgur.com/91jOLop.png" height="80%" width="80%"/>

I ran an NMAP scan at 13:48, now we will look at the logs in Discover to confirm that.

<img src="https://imgur.com/vr00j5p.png" height="80%" width="80%"/>

Using the search query process.args:”nmap”, we find an nmap scan log at 13:48. This search query will be used for the dashboard. We can click the save button on the top right to save the search query. We will call the save MyNMAP.

<img src="https://imgur.com/bKwFIMY.png" height="80%" width="80%"/>

In Dashboards, we will create a dashboard using MYNMAP. Once clicking Create Dashbord, select Add From Libary.

<img src="https://imgur.com/KVW3awD.png" height="80%" width="80%"/>


Under Create Visualization, we can create many ways to display the data.

<img src="https://imgur.com/FtT1QNE.png" height="80%" width="80%"/>

To create this specific chart, we can click Records on the left, which auto populates the axes on the right. Horizontal axis shows the time intervals, the vertical axis shows the count.

<img src="https://imgur.com/UP7zjI5.png" height="80%" width="80%"/>

The bar graph shows the number to scans every 30mins. My laptop time is 14:16. The chart shows 34 scans from 14:00.


<h2>Alerts</h2>

<img src="https://imgur.com/9hnE6YZ.png" height="80%" width="80%"/>

Under Discover, select Alerts and Create Custom Threshold Rule.

<img src="https://imgur.com/f27gXv3.png" height="80%" width="80%"/>


The alert data is auto populated. Under Equation and Threshold, I select Is Above or Equal to 1. We can scroll down to Actions to select email. 

<img src="https://imgur.com/44nZG22.png" height="80%" width="80%"/>
<img src="https://imgur.com/pkZ1505.png" height="80%" width="80%"/>

We put our email and any custom message. I’ll be leaving it on the defaults.

<img src="https://imgur.com/4QmSaIx.png" height="80%" width="80%"/>

Under Alerts and Manage Rules, we can see our rule.

<h2>Alert Testing</h2>

<img src="https://imgur.com/7Ed1hd9.png" height="80%" width="80%"/>
<img src="https://imgur.com/eQMYyWE.png" height="80%" width="80%"/>


As soon as the scan ran the email was sent to my gmail. The Alerts dashboard show the time as well.

<img src="https://imgur.com/l6bU06T.png" height="80%" width="80%"/>

