#! /bin/sh
# Dashing Dashboard init script
#
# chkconfig: 35 20 80
# description: Dashing dashboard control script

DASHING_DIR=/opt/dashboard
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games

case "$1" in
    start)
        echo "Starting Dashing"
        cd $DASHING_DIR; dashing start -d -p 80 -e production
        ;;
    stop)
        echo "Stopping Dashing"
        cd $DASHING_DIR; dashing stop
        ;;
    restart)
        cd $DASHING_DIR; bundle exec thin restart -p80 -e production
        ;;
    status)
        echo "Dashing Status"
        ps aux|grep -i dashing
        ;;
    *)
        echo "Dashing"
        echo $"Usage: $0 {start|stop|restart|status}"
        exit 1
esac
exit 0
