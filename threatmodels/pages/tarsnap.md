title: Tarsnap 
Application: Tarsnap 
date: 2014-06-06 
Trusted Parties: Local machine
Untrusted Parties: Tarsnap host, Amazon cloud servers
Key Storage: Local 
Convenience: Medium 
Authentication: HMAC-SHA256 
Architecture: Silo 
tags: [cloud][storage][backup]

# Intro

Tarsnap is a cloud-based file backup host that considers itsself very secure. "Online backups for
the truely paranoid". Data is encrypted with a key that only exists on the user's client. The data
is hosted on Amazon's E3 cloud system. The system is open source and the authors often contribute
back to the open source libraries they borrow for their system. The name comes from the archiving
tool Tar (hence the name Tarsnap), and uses very similar commands. As they claim, 'Tarsnap
compresses, encrypts, and crypto-signs every byte.' 

# Trusted Parties
Quite obviously the systems that needs to be trusted in this interaction is the user's users client
system.

# Untrusted Parties
The creator claims the biggest security risk in their system is trusting them and their code. He
says 'It's open source so you can see what's happening. But if the NSA forced me to implement a
backdoor, you'd have to find it yourself'. Another untrusted system would be Amazon since it's their
servers and cloud service that's being used. 

# Key Storage
Upon installation the user creates a keyfile, which contains two 2048-bit RSA keys, which is stored
locally and can be passphrase protected.

# Convenience
The Tarsnap program runs locally on your machine with a native command line interface. 

# Authentication
Uses two 2048-bit keys.

# Architecture
Tarsnap uses Amazon S3 storage servers which uses a cloud service to offer clients access to their
files from virtually anywhere.


