# Root Certificate Authorities

## Why?
I use self-signed CAs for internal testing and to secure privately-used services.
Also, I occasionally sign third-party services after extensive verification (for a maximum period of 180 days).

## Can I trust you?
**No.** You **cannot** trust anyone with your data. Using self-signed certificates, bad actors could perform a MITM (man-in-the-middle) attack. Please install a Certificate Authority **only** if you strongly believe the person or people behind it will not do harm.
As an example of the aforementioned issue, I'd like to introduce you to [the MITM attack of the government of Kazakhstan](https://en.wikipedia.org/wiki/Kazakhstan_man-in-the-middle_attack). Please read the Wikipedia article carefully before installing any of my as well as other third-party CAs.

## I want you to sign my certificate
First of all, thanks for your token of trust!
If you are stuck, check out the "Generate new Certificate" section in [my OpenSSL guide](https://github.com/0xb1b1/cheat-sheets/blob/main/networking/ssl/self-signed.md#generate-new-certificate).
### Ownership verification
This is how we verify ownership of your domain:
1. Generate a Certificate Signing Request for your certificate (CSR)
2. Request a random base64 string and send your CSR file
3. Create a new TXT DNS record and paste the base64 string you received
4. Ask me to verify ownership and wait for your certificate to arrive!

### Use the certificate
Replace your cert.pem file with the one you received. Done!

