## DNS: Handles naming within the Internet
reason:
 - IP addresses are hard for people to remember.
 - Use domain name is easy to migrate website, which means changing IP does no influence.
 - Readable

function: convert the names to IP addresses
a hierarchical, domain-based naming scheme and a distributed database system

resolver: a library procedure for mapping a name onto an IP (pass name as parameter)

the query and response message are UDP packets.

organization: ICANN (Internet Corporation for Assigned Names and Numbers)

hundreds of top-level domains: come in two flavors, generic and countries
non-latin alphabets were introduced in 2010.(in Arabic, Chinese..etc)
top-level domains are run by registrars appointed by ICANN.
cybersquatting: registering a domain only to turn around and sell it off to an interested party at a much higher price even has a name.

domain name is case insensitive
component names can be up to 63 chars
full path names can not exceed 255 chars.

(resource record)DNS database: five-tuple (Domain_name, Time_to_live, Class, Type, Value)

DNS can return multiple addresses for a single name.

A: ipv4
AAAA: ipv6
MX: mail exchange
NS: name server
CNAME: domain name

name resolution: look up a name and find the address
cache: 

UDP packets
DNS is a large and complex distributed system that is comprised of millions of name servers that work together
It forms a key link between human-readable domain names and the IP addresses of machines.

## E-mail
consist of : 
 - user agents: provide gui, interact with servers( compose messages and replies to messages, display incom- ing messages, and organize messages by filing, searching, and discarding)
 - message transfer agents(mail servers) 

SMTP (Simple Mail Transfer Protocol)
 - send mail over connections
 - report back the delivery status and any errors

mailboxes are maintained by mail server.

The message inside the envelope consists of two separate parts: the header and the body. The header contains control information for the user agents. The body is entirely for the human recipient.

## World Wide Web
## Multimedia
## CDN
## P2P

