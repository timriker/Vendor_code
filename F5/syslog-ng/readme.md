The following scripts will download, setup, and configure the software. <br /><br />

Getting Started: <br />

Install Attack Generator: <br /> 
<b>
  wget https://raw.githubusercontent.com/c2theg/Vendor_code/master/F5/syslog-ng/install_gen_data.sh && chmod u+x install_gen_data.sh && ./install_gen_data.sh 
</b>
<br /><br />
Update Attacks: <br />

<b> wget https://raw.githubusercontent.com/c2theg/Vendor_code/master/F5/syslog-ng/update_attacks.sh && chmod u+x update_attacks.sh && ./update_attacks.sh </b> 
<br /><br /><br /><br />




<ul>
  <li><b>Install Elastic Stack (v6): </b><br />
    wget https://raw.githubusercontent.com/c2theg/srvBuilds/master/install_elk6.sh && chmod u+x install_elk6.sh && ./install_elk6.sh

  </li>
  
  <li>
    <b>Install F5 config: </b><br />
wget https://raw.githubusercontent.com/c2theg/Vendor_code/master/F5/syslog-ng/provision.sh && chmod u+x provision.sh && ./provision.sh
  </li>
</ul>

<br /><br /><br />
To update ElasticSearch plugins, Logstash plugins, (including GeoIP databases from Maxmind) <br /><br />
 <b> sudo ./update_elk_plugins.sh  </b>


<br /><br />
Add to crontab (will update every Wednesday at 4:05am) <br /><br />
<b>  5 4 * * 3 /home/ubuntu/update_elk_plugins.sh >> /var/log/update_elk_plugins.log 2>&1  </b>


<hr />

To setup the box with a generic applications and settings: <br /> <br />

wget http://bit.ly/2wiGV4n && mv 2wiGV4n update_core.sh && chmod u+x update_core.sh && ./update_core.sh
