Title: Tahoe-LAFS
Application: Tahoe-LAFS
date: 2014-06-13
Trusted Parties: User's system
Untrusted Parties: Tahoe-LAFS servers, privileged users
Key Storage: Local by client
Convenience: Medium
Authentication: 
Architecture: Silo
tags: [cloud,storage,file,hosting]

# Intro
Tahoe-LAFS (The Least-Authority File System) is a cloud based storage solution
that operates similarly to BitTorrent, in that it distributes your storage over
several (7 default) servers.  This keeps your data available in case some of the
servers were to go down or be compromised. The files are also erasure-coded,
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
Keys are stores on the user's system.

# Convenience:
Since the customer doesn't have to deal with keys they are free from needing to
keep track of extra meticulous things, giving extra convenience to it's
customers. The program uses a CLI to interact with the files, making it not very
convenient for casual users, or very convenient for power users.

# Authentication:
The authentication is done by the gateway and the user never handles keys. The
gateway communicates with the hosting servers.

# Architecture:
The architecture for Tahoe-LAFS is federated as anyone can host their own
storage servers if they'd like.

