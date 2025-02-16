# SigScale CGF
This application provides a Charging Gateway Function (CGF) for the
collection of charging detail records (CDR) produced by Charging
Trigger Functions (CTF) in the network domains and subsystems with
presentation of normalized information on the Bx interface to a
billing domain (BD).

## Secure File Transfer Protocol (SFTP)
A jailed and hardened SFTP server is provided by this application
for CDR files to be pushed safely to the CGF. An event notification
framework may start processing pipelines on received files for
automated operation.

## CODECs
All of the 3GPP ASN.1 CDR CODECs are implemented as well as GSMA
TAP3 and some proprietary CDR. An extensible framework allows
custom callbacks for any other file formats.

## JSON Schema
The Bx interface is implemented with flexible wrap logs of JSON
objects. The Elastic Common Schema (ECS) is used for normalized
envelopes and extensive JSON Schemas describe GSMA TAP3, 3GPP CS,
PS, IMS, CHF, etc. record formats.

