
# Abstract

We are developping network address space management application. We
are collecting assigned IP address ranges and corresponding contacts
(administrative, technical and security). Assigned IP ranges do change
over time - they are changed, deleted, contacts are changed, etc. One
of scenarios for which application has been developped is as follows:
Our security team gives us single IP address and time and application
returns security contact valid at specified time. Database
includes/will include references to documentation, etc.

# Task

every assignment of IP address range starts with request form. Our
goal is to develop form as django web app. Form data will be stored in
database and e-mail will be sent.

Form (suggested type in square brackets):

Location:  network location [reference table, html dropbox]
IPv4 range: range definition (/28, /29,…)
[ dropbox, /24/24 (254), /25 (126), /26 (62), /27 (30), /28 (14), /29 (6), /30(2), /31, /32 (1) - number of usable IP addresses in round brackets]

DHCP: Yes/No - DHCP server addresses when Yes [checkbox, list of IP addresses if active]
IPv6: Yes/No - default Yes, /64 [checkbox]
DHCPv6: Yes/No - DHCP server addresses when Yes, mode stateful/stateless [checkbox, list of IPv6 addresses if active]
IPv6 RA: Yes/No [checkbox]
Firewall rules IN: rules defined for flows to newly assigned network [textarea, no check]
Firewall rules OUT: rules defined for flows from newly assigned network [textarea, no check]
Administrative contact/owner: department (as precise as possible) [reference table, dropbox]
Technical contact: contacts responsible for managing computers. [multiple emails]
Security contact: contacts responsible for security. [multiple emails]
Reverse DNS: where reverse DNS will have it's zone defined [text area, no check for now]
Network description: description of network purpose (ex: lab XY workstations) [text area, single row]


# Constraints

* HTML 5, we can use checks of email addresses... (<input type="email")
* mobile friendly app using Bootstrap http://getbootstrap.com/
* new field will be added using symbol +, new field appears
* django internationalisation
* UTF-8 coding (including source code)
* newest django (1.10)
* form will be incorporated into bigger package (think of it when developing - migrate, upgrade, etc.)
* keep README and INSTALL





