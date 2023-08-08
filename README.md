# Netdata

This collects metric data from server

## Note to setup Email config

### Getting emails on alarms

we can refer https://hub.docker.com/r/babim/netdata

Netdata supports forwarding alarms to an email address. You can set up msmtp by setting the following ENV variables:

- SMTP_TO - This is the address alarms will be delivered to.
- SMTP_FROM - This is the address the emails will be from. Defaults to localhost.
- SMTP_SERVER - This is your SMTP server. Defaults to smtp.gmail.com.
- SMTP_PORT - This is the SMTP server port. Defaults to 587.
- SMTP_USER - This is your username for the SMTP server.
- SMTP_PASS - This is your password for the SMTP server. Use an app password if using Gmail.
- SMTP_TLS - Use TLS for the connection. Defaults to on.
- SMTP_STARTTLS - Use STARTTLS for the connection. Defaults to on.

For example, using gmail:

`-e SMTP_TO=user@gmail.com -e SMTP_USER=user -e SMTP_PASS=password`

Alternatively, if you already have s msmtp config, you can use that config with:

`-v /path/to/msmtprc:/etc/msmtprc`

See the following link for details on setting up msmtp: [MSMTP - ArchWiki](https://wiki.archlinux.org/index.php/Msmtp)