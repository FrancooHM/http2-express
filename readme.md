# HTTP/2 Node.js Server Implementation with Express.js

####https://www.digitalocean.com/community/tutorials/openssl-essentials-working-with-ssl-certificates-private-keys-and-csrs

##Generate a Self-Signed Certificate from an Existing Private Key

Use this method if you already have a private key that you would like to generate a self-signed certificate with it.

This command creates a self-signed certificate (domain.crt) from an existing private key (domain.key):

openssl req \
       -key domain.key \
       -new \
       -x509 -days 365 -out domain.crt

##Private Keys
This section covers OpenSSL commands that are specific to creating and verifying private keys.

###Create a Private Key

Use this command to create a password-protected, 2048-bit private key (domain.key):

openssl genrsa -des3 -out domain.key 2048
Enter a password when prompted to complete the process.

###Verify a Private Key

Use this command to check that a private key (domain.key) is a valid key:

openssl rsa -check -in domain.key
