## init.rd script for dashing dashboard

### Configure
* mv dashingctl /etc/init.d/dashingctl
* chown +x /etc/init.d/dashingctl
* chkconfig --level 345 dashingctl on

### Verify:

        chkconfig --list dashingctl
        dashingctl     	0:off	1:off	2:off	3:on	4:on	5:on	6:off
