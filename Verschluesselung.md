# Verschlüsselung

- touch geheim.txt

## Symmetrische Verschlüsselung

- openssl rand -base64 32 > key.txt
- openssl enc -aes-256-cbc -salt -in geheim.txt -out geheim.txt.enc -pass file:key.txt
- rm geheim.txt
- openssl enc -aes-256-cbc -d -in geheim.txt.enc -out geheim.txt -pass file:key.txt

oder: 

- openssl enc -aes-256-cbc -salt -in geheim.txt -out geheim.txt.enc -pass pass:hier_kommt_ein_passwort
- openssl enc -aes-256-cbc -d -in geheim.txt.enc -out geheim_2.txt -pass pass:hier_kommt_ein_passwort

## Asymmetrische Verschlüsselung

- openssl genpkey -algorithm RSA -out private.pem
- openssl rsa -in private.pem -pubout -out public.pem
- openssl rsautl -encrypt -pubin -inkey public.pem -in geheim.txt -out geheim.txt.enc
- openssl rsautl -decrypt -inkey private.pem -in geheim.txt.enc -out geheim_2.txt

## Hashing (Einweg-Verschlüsselung)

???
- openssl dgst -sha256 geheim.txt 
- openssl dgst -sha256 -verify public.pem -signature geheim.sig geheim.txt