./clean_zabbix -h
The script deletes the old data from MySQL database that have not yet removed zabbix housekeeper. Only MySQL!!!
In other databases is not tested!

Usage:
	./clean_zabbix [options]

Options:
	-h --help			print this help
	-n --namehost=NAMEHOST		host name (h.name) in zabbix
	-m --max=MAXITEMS		max clear items
	-y --yes			yes for all (dangerous!) Use this option if you check script
	-c --connect=INFOCONNECT	host,port,user,password,database (default localhost,3306,zabbix,zabbix,zabbix)
	
Example:

1) ./clean_zabbix -c localhost,3306,zabbix,zabbix,zabbix
Check all history items. If they found outdated information on the question of removal will be asked. Is it safe to use.

2) ./clean_zabbix -c localhost,3306,zabbix,zabbix,zabbix -n server1
If they found outdated information in server1 then the question will be asked to remove. Is it safe to use.

3) ./clean_zabbix -c localhost,3306,zabbix,zabbix,zabbix -n server1 -m 5
If they found outdated information in server1 then the question will be asked to remove. It will be analyzed and processed only the first 5 items. Is it safe to use.

4) ./clean_zabbix -c localhost,3306,zabbix,zabbix,zabbix -n server1 -m 5 -y
If they found outdated information in server1 and the data will be deleted immediately. It will be analyzed and removed history only the first 5 items. Dangerous!

