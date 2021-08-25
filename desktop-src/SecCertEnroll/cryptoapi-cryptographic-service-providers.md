---
description: Les fournisseurs associés à l’API de chiffrement (CryptoAPI) sont appelés fournisseurs de services de chiffrement (CSP) dans cette documentation.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Fournisseurs de services de chiffrement CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c095fe4801cd57d4665fed0deec1649eb0a64420c13e4e5f486c7afc805447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906579"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Fournisseurs de services de chiffrement CryptoAPI

Les fournisseurs associés à l’API de chiffrement ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) sont appelés fournisseurs de services de chiffrement (CSP) dans cette documentation. Les fournisseurs de services de chiffrement implémentent généralement des algorithmes cryptographiques et fournissent un stockage de clés. Les fournisseurs associés à CNG, en revanche, l’implémentation d’algorithme distincte du stockage de clés. les fournisseurs de services de chiffrement Microsoft suivants sont distribués avec Windows Vista et Windows Server 2008.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Microsoft Base Cryptographic Provider v1.0

Implémente les algorithmes suivants pour hacher, signer et chiffrer du contenu.



| Nom                                            | Utilisation          | Type  | Taille de la clé (par défaut/min/max) |
|-------------------------------------------------|--------------|-------|----------------------------|
| Data Encryption Standard (DES)                  | Chiffrement   | Bloquer | 56/56/56                   |
| Somme de contrôle d’authentification de message haché (HMAC)   | Hashing      | Quelconque   | 0/0/0                      |
| Somme de contrôle d’authentification de message (MAC)           | Hashing      | Quelconque   | 0/0/0                      |
| Message condensé 2 (MD2)                          | Hashing      | Quelconque   | 128/128/128                |
| Message condensé 4 (MD4)                          | Hashing      | Quelconque   | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Quelconque   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Chiffrement   | Bloquer | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Chiffrement   | Bloquer | 40/40/56                   |
| Exchange de clé RSA                                | Échange de clés | RSA   | 512/384/1024               |
| Signature RSA                                   | Signature      | RSA   | 512/384/16384              |
| Algorithme de hachage sécurisé (SHA1)                    | Hashing      | Quelconque   | 160/160/160                |
| SHA (Secure Socket Layer 3) et MD5 (SSL3 SHAMD5) | Hashing      | Quelconque   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Base DSS et Diffie-Hellman fournisseur de services de chiffrement

Implémente les algorithmes suivants pour prendre en charge le hachage, la signature, le chiffrement et l’échange de clés de Diffie-Hellman.



| Nom                                  | Utilisation          | Type           | Taille de la clé (par défaut/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algorithme de chiffrement de message CYLINK   | Chiffrement   | Bloquer          | 40/40/40                   |
| Data Encryption Standard (DES)        | Chiffrement   | Bloquer          | 56/56/56                   |
| algorithme de Exchange de clé Diffie-Hellman | Échange de clés | Diffie-Hellman | 512/512/1024               |
| Algorithme éphémère Diffie-Hellman    | Échange de clés | Diffie-Hellman | 512/512/1024               |
| Algorithme de signature numérique (DSA)     | Signature      | NORME            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Quelconque            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Chiffrement   | Bloquer          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Chiffrement   | STREAM         | 40/40/56                   |
| Algorithme de hachage sécurisé (SHA1)          | Hashing      | Quelconque            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Microsoft Base DSS Cryptographic Provider

Implémente les algorithmes suivants pour signer et hacher le contenu :



| Nom                              | Utilisation     | Type | Taille de la clé (par défaut/min/max) |
|-----------------------------------|---------|------|----------------------------|
| Algorithme de signature numérique (DSA) | Signature | NORME  | 1024/512/1024              |
| Message Digest 5 (MD5)            | Hashing | Quelconque  | 128/128/128                |
| Algorithme de hachage sécurisé (SHA1)      | Hashing | Quelconque  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Microsoft Base Smart Card Crypto Provider

Prend en charge les cartes à puce et implémente les algorithmes suivants pour hacher, signer et chiffrer du contenu.

| Nom                                            | Utilisation          | Type   | Taille de la clé (par défaut/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Chiffrement   | Bloquer  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Chiffrement   | Bloquer  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Chiffrement   | Bloquer  | 256/256/256                |
| Data Encryption Standard (DES)                  | Chiffrement   | Bloquer  | 56/56/56                   |
| Triple clé DES                              | Chiffrement   | Bloquer  | 112/112/112                |
| Triple clé DES                            | Chiffrement   | Bloquer  | 168/168/168                |
| Somme de contrôle d’authentification de message haché (HMAC)   | Hashing      | Quelconque    | 0/0/0                      |
| Somme de contrôle d’authentification de message (MAC)           | Hashing      | Quelconque    | 0/0/0                      |
| Message condensé 2 (MD2)                          | Hashing      | Quelconque    | 128/128/128                |
| Message condensé 4 (MD4)                          | Hashing      | Quelconque    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Quelconque    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Chiffrement   | Bloquer  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Chiffrement   | STREAM | 128/40/128                 |
| Exchange de clé RSA                                | Échange de clés | RSA    | 1024/1024/4096             |
| Signature RSA                                   | Signature      | RSA    | 1024/1024/4096             |
| Algorithme de hachage sécurisé (SHA1)                    | Hashing      | Quelconque    | 160/160/160                |
| Algorithme de hachage sécurisé 256 (SHA256)              | Hashing      | Quelconque    | 256/256/256                |
| Algorithme de hachage sécurisé 384 (SHA384)              | Hashing      | Quelconque    | 384/384/384                |
| Algorithme de hachage sécurisé 512 (SHA512)              | Hashing      | Quelconque    | 512/512/512                |
| SHA (Secure Socket Layer 3) et MD5 (SSL3 SHAMD5) | Hashing      | Quelconque    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Fournisseur de services de chiffrement Microsoft DH SChannel

Prend en charge le package de sécurité Secure Channel (SChannel) qui implémente les protocoles d’authentification SSL (Secure Sockets Layer) (SSL) et TLS (Transport Layer Security). Ce fournisseur CSP prend également en charge l’échange de clés de Diffie-Hellman et implémente les algorithmes suivants.



| Nom                                   | Utilisation                | Type           | Taille de la clé (par défaut/min/max) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algorithme de chiffrement de message CYLINK    | Chiffrement         | Bloquer          | 40/40/40                   |
| Data Encryption Standard (DES)         | Chiffrement         | Bloquer          | 56/56/56                   |
| Triple clé DES                     | Chiffrement         | Bloquer          | 112/112/112                |
| Triple clé DES                   | Chiffrement         | Bloquer          | 168/168/168                |
| algorithme de Exchange de clé Diffie-Hellman  | Échange de clés       | Diffie-Hellman | 512/512/4096               |
| Algorithme éphémère Diffie-Hellman     | Échange de clés       | Diffie-Hellman | 512/512/4096               |
| Algorithme de signature numérique (DSA)      | Signature            | NORME            | 1024/512/1024              |
| Message Digest 5 (MD5)                 | Hashing            | Quelconque            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Chiffrement         | Bloquer          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Chiffrement         | STREAM         | 40/40/128                  |
| Algorithme de hachage sécurisé (SHA1)           | Hashing            | Quelconque            | 160/160/160                |
| Clé de chiffrement Schannel                | Chiffrement         | Schannel       | 0/0/-1                     |
| Clé MAC Schannel                       | Chiffrement/hachage | Schannel       | 0/0/-1                     |
| Hachage principal Schannel                   | Chiffrement/hachage | Schannel       | 0/0/-1                     |
| Maître SSL (Secure Sockets Layer) (SSL3)     | Chiffrement         | Schannel       | 384/384/384                |
| Master TLS1 (Transport Layer Security) | Chiffrement         | Schannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Microsoft Enhanced Cryptographic Provider v1.0

Offre une sécurité renforcée par rapport au fournisseur de services de chiffrement de base Microsoft v 1.0 en utilisant des clés plus longues avec certains des algorithmes existants et en implémentant des algorithmes supplémentaires.



| Nom                                            | Utilisation          | Type   | Taille de la clé (par défaut/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Chiffrement   | Bloquer  | 56/56/56                   |
| Triple clé DES                              | Chiffrement   | Bloquer  | 112/112/112                |
|                                                 | Chiffrement   | Bloquer  | 168/168/168                |
| Somme de contrôle d’authentification de message haché (HMAC)   | Hashing      | Quelconque    | 0/0/0                      |
| Somme de contrôle d’authentification de message (MAC)           | Hashing      | Quelconque    | 0/0/0                      |
| Message condensé 2 (MD2)                          | Hashing      | Quelconque    | 128/128/128                |
| Message condensé 4 (MD4)                          | Hashing      | Quelconque    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Quelconque    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Chiffrement   | Bloquer  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Chiffrement   | STREAM | 128/40/128                 |
| Exchange de clé RSA                                | Échange de clés | RSA    | 1024/384/16384             |
| Signature RSA                                   | Signature      | RSA    | 1024/384/16384             |
| Algorithme de hachage sécurisé (SHA1)                     | Hashing      | Quelconque    | 160/160/160                |
| SHA (Secure Socket Layer 3) et MD5 (SSL3 SHAMD5) | Hashing      | Quelconque    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS et Diffie-Hellman fournisseur de services de chiffrement

Offre une sécurité renforcée par rapport aux fournisseurs de services de chiffrement DSS de base Microsoft et Diffie-Hellman en utilisant des clés plus longues avec certains des algorithmes existants et en implémentant des algorithmes supplémentaires.



| Nom                                  | Utilisation          | Type           | Taille de la clé (par défaut/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algorithme de chiffrement de message CYLINK   | Chiffrement   | Bloquer          | 40/40/40                   |
| Data Encryption Standard (DES)        | Chiffrement   | Bloquer          | 56/56/56                   |
| Triple clé DES                    | Chiffrement   | Bloquer          | 112/112/112                |
| Triple clé DES                  | Chiffrement   | Bloquer          | 168/168/168                |
| algorithme de Exchange de clé Diffie-Hellman | Échange de clés | Diffie-Hellman | 1024/512/4096              |
| Algorithme éphémère Diffie-Hellman    | Échange de clés | Diffie-Hellman | 1024/512/4096              |
| Algorithme de signature numérique (DSA)     | Signature      | NORME            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Quelconque            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Chiffrement   | Bloquer          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Chiffrement   | STREAM         | 128/128/128                |
| Algorithme de hachage sécurisé (SHA1)          | Hashing      | Quelconque            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Fournisseur de services de chiffrement RSA et AES amélioré Microsoft

Implémente les algorithmes suivants pour signer, chiffrer et hacher du contenu.



| Nom                                            | Utilisation          | Type   | Taille de la clé (par défaut/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Chiffrement   | Bloquer  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Chiffrement   | Bloquer  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Chiffrement   | Bloquer  | 256/256/256                |
| Data Encryption Standard (DES)                  | Chiffrement   | Bloquer  | 56/56/56                   |
| Triple clé DES                              | Chiffrement   | Bloquer  | 112/112/112                |
| Triple clé DES                            | Chiffrement   | Bloquer  | 168/168/168                |
| Somme de contrôle d’authentification de message haché (HMAC)   | Hashing      | Quelconque    | 0/0/0                      |
| Somme de contrôle d’authentification de message (MAC)           | Hashing      | Quelconque    | 0/0/0                      |
| Message condensé 2 (MD2)                          | Hashing      | Quelconque    | 128/128/128                |
| Message condensé 4 (MD4)                          | Hashing      | Quelconque    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Quelconque    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Chiffrement   | Bloquer  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Chiffrement   | STREAM | 128/128/128                |
| Exchange de clé RSA                                | Échange de clés | RSA    | 1024/384/16384             |
| Signature RSA                                   | Signature      | RSA    | 1024/384/16384             |
| Algorithme de hachage sécurisé (SHA1)                    | Hashing      | Quelconque    | 160/160/160                |
| Algorithme de hachage sécurisé (SHA256)                  | Hashing      | Quelconque    | 256/256/256                |
| Algorithme de hachage sécurisé (SHA384)                  | Hashing      | Quelconque    | 384/384/384                |
| Algorithme de hachage sécurisé (SHA512)                  | Hashing      | Quelconque    | 512/512/512                |
| SHA (Secure Socket Layer 3) et MD5 (SSL3 SHAMD5) | Hashing      | Quelconque    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Fournisseur de services de chiffrement Microsoft RSA Schannel

Prend en charge le package de sécurité RSA Secure Channel (SChannel) qui implémente les protocoles d’authentification SSL (Secure Sockets Layer) (SSL) et TLS (Transport Layer Security).



| Nom                                            | Utilisation                | Type     | Taille de la clé (par défaut/min/max) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Chiffrement         | Bloquer    | 128/128/128                |
| Advanced Encryption Standard 256 (AES256)       | Chiffrement         | Bloquer    | 256/256/256                |
| Data Encryption Standard (DES)                  | Chiffrement         | Bloquer    | 56/56/56                   |
| Triple clé DES                              | Chiffrement         | Bloquer    | 112/112/112                |
| Triple clé DES                            | Chiffrement         | Bloquer    | 168/168/168                |
| Somme de contrôle d’authentification de message haché (HMAC)   | Hashing            | Quelconque      | 0/0/0                      |
| Somme de contrôle d’authentification de message (MAC)           | Hashing            | Quelconque      | 0/0/0                      |
| Message Digest 5 (MD5)                          | Hashing            | Quelconque      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Chiffrement         | Bloquer    | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Chiffrement         | STREAM   | 128/128/128                |
| Exchange de clé RSA                                | Échange de clés       | RSA      | 1024/384/16384             |
| Clé de chiffrement Schannel                         | Chiffrement         | Schannel | 0/0/-1                     |
| Hachage principal Schannel                            | Chiffrement/hachage | Schannel | 0/0/-1                     |
| Clé MAC Schannel                                | Chiffrement/hachage | Schannel | 0/0/-1                     |
| Algorithme de hachage sécurisé (SHA1)                    | Hashing            | Quelconque      | 160/160/160                |
| Maître SSL (Secure Socket Layer 2) (SSL2)             | Chiffrement         | Schannel | 40/40/192                  |
| Maître SSL3 (Secure Socket Layer 3)             | Chiffrement         | Schannel | 384/384/384                |
| SHA (Secure Socket Layer 3) et MD5 (SSL3 SHAMD5) | Hashing            | Quelconque      | 288/288/288                |
| Master TLS1 (Transport Layer Security)          | Chiffrement         | Schannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Microsoft Strong Cryptographic Provider

Implémente les algorithmes suivants.



| Nom                                            | Utilisation          | Type   | Taille de la clé (par défaut/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Chiffrement   | Bloquer  | 56/56/56                   |
| Triple clé DES                              | Chiffrement   | Bloquer  | 112/112/112                |
| Triple clé DES                            | Chiffrement   | Bloquer  | 168/168/168                |
| Somme de contrôle d’authentification de message haché (HMAC)   | Hashing      | Quelconque    | 0/0/0                      |
| Somme de contrôle d’authentification de message (MAC)           | Hashing      | Quelconque    | 0/0/0                      |
| Message condensé 2 (MD2)                          | Hashing      | Quelconque    | 128/128/128                |
| Message condensé 4 (MD4)                          | Hashing      | Quelconque    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Quelconque    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Chiffrement   | Bloquer  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Chiffrement   | STREAM | 128/40/128                 |
| Exchange de clé RSA                                | Échange de clés | RSA    | 1024/384/16384             |
| Signature RSA                                   | Signature      | RSA    | 1024/384/16384             |
| Algorithme de hachage sécurisé (SHA1)                    | Hashing      | Quelconque    | 160/160/160                |
| SHA (Secure Socket Layer 3) et MD5 (SSL3 SHAMD5) | Hashing      | Quelconque    | 288/288/288                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comprendre les fournisseurs de services de chiffrement](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
