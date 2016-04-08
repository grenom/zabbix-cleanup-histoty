The perl script deletes the old data from MySQL database that have not yet removed zabbix housekeeper. Only MySQL!!!
In other databases is not tested!
For details read --help output.

Needed to work:
perl
use DBI
use Term::ANSIColor
use Time::HiRes
use Getopt::Long
