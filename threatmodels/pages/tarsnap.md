title: Tarsnap
Application: Tarsnap
date: 2014-06-06
Trusted Parties: Local machine
Untrusted Parties: -other
Key Storage: Local
Convenience: Medium
Authentication: HMAC-SHA256
Architecture: -other
tags: [cloud][storage][backup]

# Intro

Tarsnap is a cloud-based file backup host that considers itsself very secure. Data is encrypted
with a key that only exists on the user's client. The data is hosted on Amazon's E3 cloud system.
The system is open source and the authors often contribute back to the open source libraries they
borrow for their system. The name comes from the archiving tool Tar (hence the name Tarsnap), and
uses very similar commands. As they claim, 'Tarsnap compresses, encrypts, and crypto-signs every
byte.' 

# Trusted Parties
Quite obviously the systems that need to be trusted in this interaction are the user's users
client system and the Tarsnap host. The creator claims the biggest security risk in their system
is trusting them and their code. He says 'It's open source so you can see what's happening. But if
the NSA forced me to implement a backdoor, you'd have to find it yourself'. You would also have to
trust Amazon since it's their cloud service that's being used. 

# Untrusted Parties


# Key Storage
Upon installation the user creates a keyfile, which contains two 2048-bit RSA keys, which is
stored locally and can be passphrase protected.

# Convenience
The Tarsnap program runs locally on your machine with a native command line interface. 

# Authentication
Uses two 2048-bit keys.

# Architecture





#####
notes
#####

"Secure" online backup service for Unix-like systems.
Encrypts and stores data on Amazon E3 (Cloud, man)
"Security Keys are only known to user" - John Callas recomends Tarsnap
- Open Source
- Porivdes a command line client
Works like tar but with cloud-based archives
Tarsnap compresses, encrypts, and crypto-signs every byte.
During installation the user creates a keyfile, which can be optionally passphrase protected.
	The file contains two 2048-bit RSA keys, Uses HMAC-SHA-256 hash to verify data.
	Same hash used to verify client - server commiunication. 
Only files that have changed are backedup.
Tarsnap charges only for the data / bandwidth they use.
30cents / GB stored and 30cents GB transmeitted.
Charges based on quintillionth of a dollar (18 decimal places)
Easy to script
Open source license
They use open source libraries, and contribute back to them. 
Offers bug bounties
Creator: Dr. Colin Percival, ex FreeBSD Security Officer
Weakest link is the coder(s).



