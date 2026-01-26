A Clinic that only Requires 5 Computers in IT for telemedication, 2 For Registration, and 3 computers for Finance Department.
The Network Address they use is : 10.0.0.0/24
<img width="1148" height="552" alt="image" src="https://github.com/user-attachments/assets/81f7e8ad-bece-4452-9d5f-1ba088c01e4e" />


After VLSM the IP for<br>
IT: 10.0.0.1/29, .2, .3, .4, .5, .6, .7<br>
Finance: 10.0.0.9/29, .10, .11, .12, .13, .14, .15<br>
Registration: 10.0.0.17/30, .18, .19<br>
<br>
Setting VLAN Names:<br>
IT → VLAN 10<br>
Finance → VLAN 20<br>
Registration → VLAN 30<br>
<br>
Switch><br>
Switch> enable<br>
Switch# config t<br>
Enter configuration commands, one per line. End with CNTL/Z.<br>
Switch(config)# vlan 10<br>
Switch(config-vlan)# name IT<br>
Switch(config-vlan)# exit<br>
Switch(config)# vlan 20<br>
Switch(config-vlan)# name FINANCE<br>
Switch(config-vlan)# exit<br>
Switch(config)# vlan 30<br>
Switch(config-vlan)# name REGISTRATION<br>
Switch(config-vlan)# exit<br>
<br>
Commands to give access to each port to the VLANs:<br>
<br>
interface fa0/1<br>
switchport mode access<br>
switchport access vlan 30<br>
exit<br>
<br>
interface fa0/2<br>
switchport mode access<br>
switchport access vlan 30<br>
exit<br>
<br>
Note: Do this for all the 10 ports fa0/1 to fa0/10 to their respective VLANs.<br>
Figure below shows the assignments is successful.<br>
<br>
Note: In case of wrong VLAN assignment, go to the interface and enter:<br>
no switchport mode access<br>
Example:<br>
interface fa0/1 → no switchport mode access<br>
<img width="783" height="496" alt="image" src="https://github.com/user-attachments/assets/f7030dfe-0172-4ebc-aae0-3573ac32b17a" />


