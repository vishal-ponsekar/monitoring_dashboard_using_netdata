# Simple Monitoring
Set up a basic monitoring dashboard using Netdata.

### Steps I followed
- Created an ubuntu ec2 instance in aws.
- Installed Netdata agent in that instance using kickstart.sh file.
- If you want to install in the same way use the following doc.
  https://learn.netdata.cloud/docs/netdata-agent/installation/linux/#run-the-one-line-install-command
- After, installed netdata allowed 19999 port in security group of the instance to see the netdata agent console.
- Next, tried to see the console using public_ip_of_server:19999. It took me to the netdata agent console. Initially it asks to signin I chose the skip and use the dashboard anonymously option.
- After, chose the dashboard anonymously option it will shows the metrics of the instance.
- There, to check the CPU utilization metric. I installed stress in the instance to create CPU hike.
- Use the following command to create the CPU hike.
  
  ```bash
  stress --cpu 1 --timeout 300
  ```
  --timeout 300 is the CPU hike will happen only 300 seconds means 5 minutes.
- Then, I added system cpu utilization chart in the local-custom-dashboard from dashboard tab. And renamed the dashboard.
  
![loading...](images/netdata-dashboard.png)
