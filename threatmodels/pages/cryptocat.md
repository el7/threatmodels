title: Cryptocat
Application: Cryptocat 
date: 2014-06-13
Trusted Parties: Local, friend
Untrusted Parties: Remote website
Key Storage: Local
Convenience: Medium
Authentication: Challenge request Auth
Architecture: Federated
tags: [chat,messaging,XMPP,OTR]


# Intro
Cryptocat is a browser-based instant messaging program that offers client side
encryption. The client is loaded locally as a browser extension for Google Chrome
or Mozilla Firefox, and communicates to an XMPP-BOSH sever over HTTPS. Cryptocat
runs on the OTR (Off the Record) protocol for two-party encryption conversations
and the mpOTR for multi-party encrypted conversations.

# Trusted Parties
Since this is a browser extension the code runs locally on each computer. The
trusted parties would include each user that's using the extension. You also need
to assume that your browser isn't compromised or that you don't have any
malicious extensions installed alongside of Cryptocat. You must also trust the OTR
and mpOTR protocols.

# Untrusted Parties
User messages are encrypted before they are sent from your browser, thus not
needing to trust a specific website. 

# Key Storage
The browser extension generates (mp/OTR) key pairs, encrypts, sends, receives and
decrypts messages, sends and receives [mp]OTR public keys, and calculates the
public key footprints. 

# Convenience
Cryptocat offers encrypted messaging directly from a browser extension. This is a
convenient method of communication over the Off The Record protocol, but doesn't
serve much purpose when there isn't a network connection available. It's also
impossible to disable OTR as unencrypted messages are rejected by the server. 

# Authentication
A chat room visitor provides the Cryptocat service with a room name and
nickname. Cryptocat then generates an OTR key pair (public and private), and
then generates an XMPP username and password. These are used to register a new
user on the server. The visitor then sends their public OTR key to the XMPP
server, which returns a challenge to the Cryptocat OTR key in order to prove
that Cryptocat owns the private key to the offered public key. If the challenge
is successful, the XMPP server assigns an XMPP identity to the user based on
their public key. An mpOTR key exchange then occurs between the users, which is
where their username is exchanged, never seen by the XMPP server.


# Architecture
The two systems include the client systems (at least two separate parties) and
the relay systems (the XMPP and BOSH servers), making this a federated
architecture.

