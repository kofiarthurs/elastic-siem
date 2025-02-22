<h1>Elastic SIEM</h1>
<h2>Description</h2>
In today’s lab, We will set up ELK to monitor our Kali machine for nmap scans and send email alerts.

<h2>Deployment Option</h2>

On signing up, select Elastic for Observability. I named my project MySiemLAB.

Opening the deployment leads to the dashboard where we will be doing the next steps below.

<h2>Integrations</h2>

Once everything was configured, select Integrations under Management and chose Elastic Defend.


Click on Install Elastic Agent. The image below shows the installation options.

I selected Linux Tar for my Kali Machine. Once installed, you will get a confirmation under Confirm Agent Enrollment.


Under Fleet, we can see my Kali machine.

<h2>Discover & Dashboards</h2>

I ran an NMAP scan at 13:48, now we will look at the logs in Discover to confirm that.

Using the search query process.args:”nmap”, we find an nmap scan log at 13:48. This search query will be used for the dashboard. We can click the save button on the top right to save the search query. We will call the save MyNMAP.


In Dashboards, we will create a dashboard using MYNMAP. Once clicking Create Dashbord, select Add From Libary.


Under Create Visualization, we can create many ways to display the data.

To create this specific chart, we can click Records on the left, which auto populates the axes on the right. Horizontal axis shows the time intervals, the vertical axis shows the count.

The bar graph shows the number to scans every 30mins. My laptop time is 14:16. The chart shows 34 scans from 14:00.


<h2>Alerts</h2>


Under Discover, select Alerts and Create Custom Threshold Rule.


The alert data is auto populated. Under Equation and Threshold, I select Is Above or Equal to 1. We can scroll down to Actions to select email. 


We put our email and any custom message. I’ll be leaving it on the defaults.


Under Alerts and Manage Rules, we can see our rule.

<h2>Alert Testing</h2>



As soon as the scan ran the email was sent to my gmail. The Alerts dashboard show the time as well.

