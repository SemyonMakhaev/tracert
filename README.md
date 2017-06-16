# The tracert utility

## The traceroute utility for a route from a current host to the destination address tracing.

The program sends echo-ICMP requests with TTL = 1, 2, ... K to each of destination
addresses where K is an ordering number of a package achieved the destination. It
recieves ICMP-packages with code 11 (TTL exceeded) and gets an IP-address of a transitional
host. Also the program sends requests to the WHOIS-server for counry, network name and
an autonomic system number of a current host getting. As default there is set
whois.iana.org server. If a WHOIS-reply includes a reference to another WHOIS-server
than the program sends a one more request to this server for an information getting.

User can set any number of destination addresses as program arguments. Also he can
set a maximal hopes count else it will be a default value. Use -h or --help for
a help message calling.

A RAW-socket is using for ICMP-request assembling so that user should have
administrator privileges. A request assembling realized by the struct module.
