title: PGP
Application: PGP
date: 2014-06-09
Trusted Parties: Local Machine
Untrusted Parties: Any intermediary
Key Storage: Local
Convenience: Low
Authentication: Web of Trust
Architecture: federated
tags: [email]

# Intro

PGP is a method of end-to-end encryption for email using public key
cryptography. At the time of composing a new message, the sender must have the
public keys of all intended recipients. The sender must also have a private
key so that they can sign the encrypted message. Using PGP means messages are
encrypted before being sent to any server handling the message. It is not
possible for the message to be decrypted by anyone except for the intended
recipients. Overall, PGP offers very strong security properties and is one of
the oldest and most highly regarded methods of encryption.

# Trusted Parties

The local machine of the sender and the recipient(s) need to be trusted in
order for the security properties of PGP to be maintained. Further, the
ownership of the public keys must be verified properly.  If an untrustworthy
public key is used, the exchange is vulnerable to a man-in-the-middle attack.

# Untrusted Parties

Any entity handling a message encrypted with PGP does not need to be trusted.

# Key Storage

Keys are stored locally, or any arbitrary location of the user's choosing. The
PGP protocol does not require keys to be stored in a particular location.

# Convenience

As mentioned below, the biggest sore spot of PGP is authentication. While the
web of trust is effective in small groups, it does not scale well and can be
compromised by taking advantage of less than rigorous participants.

In addition to the authentication problem, nearly every implementation of PGP
requires manually copying and pasting encrypted messages into existing email
solutions. Further reducing convenience is needing to know the public key of
the recipient before being able to encrypt and send the message.

Notably Thunderbird with the Enigmail extension makes PGP quite usable.
However, Thunderbird is not actively developed. Further, this combination does
not solve the problem of a recipient needing to use PGP in order to receive an
encrypted message.

For these reasons, the convenience of PGP is listed as low.

# Authentication

Authentication of PGP is done via the web of trust. A key becomes trusted after
it is signed by a key which is already trusted. Assuming that all identities
are properly verified before signing, this system is fairly robust in small
groups.  However, if control of a private key is compromised then a malicious
party may sign keys to exploit the web of trust. 

Key revocation is a method of mitigating this scenario. However, it is not
possible to revoke a key without possession of the private key. If the private
key is lost or if the owner of the compromised key does not realize they have
been compromised, key revocation is not effective.

# Architecture

PGP is designed to interface with existing mail protocols. The architecture of
PGP is considered federated since anyone can host an email server that can
accept PGP messages.
