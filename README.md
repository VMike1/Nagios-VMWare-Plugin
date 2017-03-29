# Nagios-VMWare-Plugin
This script is plugin for Nagios. It checks some metrics through VMWare VCenter server.

The scripts runs in two modes.
'Server' mode gets login to VMWare from stdio and works as interface to VCenter.
'Client' mode used for nagios commands gets metrics from running 'server' module.

This separate architecture intended for avoiding password storage in NAGIOS configuration files.
The VCenter's password typed at 'server' module start and not stored anywhere. This 'server'
module works until killed externally and handles requests from Nagios through 'client' module.
