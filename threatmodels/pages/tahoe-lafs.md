#Title: Tahoe-LAFS
Application: Tahoe-LAFS
date: 2014-06-13
Trusted Parties: User's system
Untrusted Parties: Tahoe-LAFS servers, privledged users
Key Storage: Doesn't use keys
Convenience: Medium
Authentication: 
Architecture: P2P
tags: cloud,storage,file,hosting

# Intro
Tahoe-LAFS (The Least-Authority File System) is a cloud based storage solution
that operates similarly to BitTorrent, in that it distributes your storage over
several (7 default) servers.  This keeps your data avaiable in case some of the
servers were to go down ot be compromised. The files are also erasure-coded,
which is a form of bit recovery.

# Trusted Parties: 
The files are secured with what they call "provider-independent", where the
gateway (user client) encrypts the files before they are sent to the "nodes". In
this case it's the user's system that needs to be trusted. The files are stored
on a "storage grid" which is made up of a number of storage servers. The client
acts as the gateway for the storage nodes.

# Untrusted Parties:
The untrusted parties would be the Tahoe-LAFS program, and the servers they use
to distribute the data. There is also a feature that lets the user pick
individuals to have read or read/write access, who can also grant read or
read/write access to others. 

# Key Storage:
The authenitication is done by the gateway and the user never handles keys. The
gateway communicates with the hosting servers, giving the clients freedom of
convinience. 


# Convenience:
Since the customer doesn't have to deal with keys they are free from needing to
keep track of extra meticulous things, giving extra convinience to it's
customers. 

# Authentication:
Unsure how authenication works ...

# Architecture:
The user's files are broken up and stored on several distributed servers, using
a P2P structure between each server.

