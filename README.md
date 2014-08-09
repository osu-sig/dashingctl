## init.rd script for dashing dashboard

### Assumptions
* You have a rhel system (we are using chkconfig in configure section)
* You only have dashing (thin) running on port 80. If this is not true you will need to modify status 

### Configure 
* edit dashingctl and update DASHING_DIR variable to point at your dashboard directory
* cp dashingctl /etc/init.d/dashingctl
* chmod 0755 /etc/init.d/dashingctl
* chkconfig --add dashingctl
* chkconfig --level 345 dashingctl on

### Verify:

        chkconfig --list dashingctl
        dashingctl     	0:off	1:off	2:off	3:on	4:on	5:on	6:off
        
