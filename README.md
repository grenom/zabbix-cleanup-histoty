The perl script deletes the old data from MySQL database that have not yet removed zabbix housekeeper. Only MySQL!!!
In other databases is not tested!
For details read --help output.

Tested on Zabbix server v2.4.7 (revision 56694) (12 November 2015)

Needed to work:
perl
use DBI
use Term::ANSIColor
use Time::HiRes
use Getopt::Long
