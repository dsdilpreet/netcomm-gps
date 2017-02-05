## Description
Shell Script which saves the GPS data to a CSV file in Micro SD card for NetComm Wireless NTC-140 and NTC-140W routers.

### Copying and Executing Script
Download and move the script file (`cgps.template`) to `/etc/cdcs/conf/mgr_templates` directory of the router and give it executable permissions by running `chmod +x cgps.template` command. The script should create a `gps.csv` file in your Micro SD card located at `/var/mnt/SDDisk0P1/` directory of the router with GPS data.

### Flow of Script
Script saves the GPS latitude and longitude coordinates in the file if the cordinates differ by certain distance (in this example 5 meters). Flow chart is attached below:

![Image of flow chart](https://raw.githubusercontent.com/dsdilpreet/netcomm-gps/master/Docs/flow_chart.png)

### What does the `gps.csv` file contain?
Sample `gps.csv` output is attached below:

![Image of sample output](https://raw.githubusercontent.com/dsdilpreet/netcomm-gps/gh-pages/Docs/sample_ouput.png)

Each column represents following data:

Column | Description
------------ | -------------
A | Date formatted in `day/month/year`
B | Time formatted in `hour/minute/second`
C | Latitude Coordinates
D | Longitude Coordinates
E | Number of sattelites used to gather the data
F | Source of GPS data. Possible values are `standalone` or `agps` (assisted GPS)
