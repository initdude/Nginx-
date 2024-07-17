# Nginx
Setup Nginx Project with self-sign SSL Certification
it's just a sample, beause of privacy i didn't add full addresses.



Overview

This project sets up an Nginx server with a self-signed SSL certificate.

Prerequisites

OpenSSL installed Nginx installed

Steps to Generate a Self-Signed Certificate

Generate a private key:

openssl genpkey -algorithm RSA -out private.key

Create a Certificate Signing Request (CSR):

openssl req -new -key private.key -out csr.csr

Generate the self-signed certificate:

openssl x509 -req -days 365 -in csr.csr -signkey private.key -out certificate.crt
