# DynDNS-bash
Update Dynamic DNS on GoDaddy through API

OP: https://www.instructables.com/Quick-and-Dirty-Dynamic-DNS-Using-GoDaddy/

Create a new A record in GoDaddy pointing to any IP address.

Obtain API Key for your GoDaddy account.

Save file at /usr/local/sbin/gd-dyndns and do a chmod 700 to secure it.

Update domain, hostname and API key:secret on the script.

To set it as a cronjob every 10 minutes:

	sudo crontab -e

Append at the end of the file:
		
	*/10 * * * *    /usr/local/sbin/gd-dyndns > /dev/null
