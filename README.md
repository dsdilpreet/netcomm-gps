<h2>Description</h2>
Shell Script which saves the GPS data to a CSV file in Micro SD card for NetComm Wireless NTC-140 and NTC-140W routers.

<h3>Copying and Executing Script</h3>
Copy this script file to <code>/etc/cdcs/conf/mgr_templates</code> directory of the router and give it executable permissions by running <code>chmod +x cgps.template</code> command. The script should create a <code>gps.csv</code> file in your Micro SD card located at <code>/var/mnt/SDDisk0P1/</code> directory of the router.

<h3>Additional Info for file in Dev branch</h3>
Script now saves data to <code>gps.csv</code> file in Micro SD card when latitude changes by certain distance (in this case - 1.11 metres North).
