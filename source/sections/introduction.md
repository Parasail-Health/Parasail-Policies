# Introduction

Parasail, Inc ("Parasail") is committed to ensuring the confidentiality, privacy, integrity, and availability of all electronic protected health information (ePHI) it receives, maintains, processes and/or transmits on behalf of its Customers. As providers of compliant, hosted infrastructure used by health technology vendors, developers, designers, agencies, custom development shops, and enterprises, Parasail strives to maintain compliance, proactively address information security, mitigate risk for its Customers, and assure known breaches are completely and effectively communicated in a timely manner. The following documents address core policies used by Parasail to maintain compliance and assure the proper protections of infrastructure used to store, process, and transmit ePHI for Parasail Customers.

## Parasail Organizational Concepts

The physical infrastructure environment is hosted at [Amazon Web Services](https://aws.amazon.com/) (AWS). The network components and supporting network infrastructure are contained within and managed by AWS. Parasail does not have physical access into the network components. The Parasail environment consists of Cisco firewalls, Apache web servers, PostgreSQL database servers, Logstash logging servers, Linux Ubuntu monitoring servers, OSSEC IDS services, Docker containers, and developer tools servers running on Linux Ubuntu.

Within the Parasail Platform on AWS, all data transmission is encrypted and all hard drives are encrypted so data at rest is also encrypted; this applies to all servers - those hosting Docker containers, databases, APIs, log servers, etc. Parasail assumes all data *may* contain ePHI, even though our Risk Assessment does not indicate this is the case, and provides appropriate protections based on that assumption.

The bastion host, Apache web server are externally facing and accessible via the Internet. The database servers, where the ePHI resides, are located on the internal Parasail network and can only be accessed directly over an SSH connection through the bastion host. The access to the internal database is restricted to a limited number of personnel and strictly controlled to only those personnel with a business justified reason. Remote access to the internal servers is not accessible except through the load balancers and bastion host.

## Version Control

Policies were last updated October 25th, 2016.
