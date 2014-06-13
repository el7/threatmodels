title: Cryptocat
Application: Cryptocat 
date: 2014-06-13
Trusted Parties: Local, friend
Untrusted Parties: Remote website
Key Storage: Local
Convenience: Medium
Authentication: Challenge request Auth
Architecture: Federated
tags: chat,messaging,XMPP,OTR


# Intro
Cryptocat is a browser-based instant messaging program that offers client side
encryption. The client is loaded locally as a browser plugin for Google Chrome
or Mozilla Firefox, and communicates to an XMPP-BOSH sever over HTTPS. Cryptocat
runs on the OTR (Off the Record) protocol for two-party encryption conversations
and the mpOTR for multi-party encrypted conversations.

# Trusted Parties
Since this is a browser plugin the code runs locally on each computer. The
trusted parties would include each user that's using the pluglin. You also need
to assume that your browser isn't compromised or that you don't have any
malicious plugins installed alongside of Cryptocat. You must also trust the OTR
and mpOTR protocols.

# Untrusted Parties
User messages are encrypted before they are sent from your browser, thus not
needing to trust a specific website. 

# Key Storage
The browser plugin generates (mp/OTR) key pairs, encrypts, sends, recieves and
decrypts messages, sends and recieves [mp]OTR public keys, and calculats the
public key footprints. 

# Convenience
Cryptocat offers encrypted messaging directly from a browser plugin. This is a
convinient method of comminication over the Off The Record protocol, but doesn't
serve much purpose when there isn't a network connection availible. It's also
impossible to disable OTR as unencrypted messages are rejected by the server. 

# Authentication
The system uses a challenge repsonse for the Cryptocat OTR key in order to prove
that Cryptocat owns the private key to the offered public key. If answered
successfully, the XMPP server offers an identity to the user based on their
public key. 

# Architecture
The two systems include the client systems (at least two seperate parties) and
the relay systems (the XMPP and BOSH servers), making this a federated
architecture. 


