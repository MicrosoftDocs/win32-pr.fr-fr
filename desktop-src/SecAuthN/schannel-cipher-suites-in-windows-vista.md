---
description: Ensemble d’algorithmes de chiffrement. Les protocoles Schannel utilisent des algorithmes à partir d’une suite de chiffrement pour créer des clés et chiffrer des informations.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Suites de chiffrement TLS dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cf270f0608666b7d766e3f063f24ea39204fd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311333"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Suites de chiffrement TLS dans Windows Vista

Une suite de chiffrement est un ensemble d’algorithmes de chiffrement. Les protocoles Schannel utilisent des algorithmes à partir d’une suite de chiffrement pour créer des clés et chiffrer des informations. Une suite de chiffrement spécifie un algorithme pour chacune des tâches suivantes :

-   Échange de clés
-   Chiffrement en bloc
-   Authentification de message

Les [*algorithmes d’échange de clés*](../secgloss/k-gly.md) protègent les informations requises pour créer des clés partagées. Ces algorithmes sont asymétriques ([*algorithmes de clé publique*](../secgloss/p-gly.md)) et fonctionnent bien pour des quantités de données relativement petites.

Les algorithmes de chiffrement en bloc chiffrent les messages échangés entre les clients et les serveurs. Ces algorithmes sont [*symétriques*](../secgloss/s-gly.md) et fonctionnent correctement pour de grandes quantités de données.

Les algorithmes [d’authentification de message](message-authentication-codes-in-schannel.md) génèrent des [*hachages*](../secgloss/h-gly.md) de message et des signatures qui garantissent l' [*intégrité*](../secgloss/i-gly.md) d’un message.

Les développeurs spécifient ces éléments à l’aide des types de données d' [**\_ ID ALG**](../seccrypto/alg-id.md) . Pour plus d’informations, consultez [spécification des chiffrements Schannel et des niveaux de chiffrement](specifying-schannel-ciphers-and-cipher-strengths.md).

Schannel prend en charge les suites de chiffrement suivantes. Les suites sont répertoriées dans l’ordre par défaut dans lequel elles sont choisies par le fournisseur Microsoft Schannel.

> [!IMPORTANT]
> Les services Web HTTP/2 échouent avec les suites de chiffrement compatibles non-HTTP/2. Pour garantir la fonction de vos services Web avec les clients et les navigateurs HTTP/2, consultez Guide pratique [pour déployer le classement personnalisé des suites de chiffrement](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 



| Suite de chiffrement                                                 | Mode FIPS activé | Exchange              | Chiffrement      | Hachage            | Protocoles                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                | Oui<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                | Oui<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ RC4 \_ 128 \_ SHA<br/>                     | Non<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ 3DES \_ Ede \_ CBC \_ SHA<br/>               | Oui<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/> | Oui<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/> | Oui<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/> | Oui<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/> | Oui<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/> | Oui<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/> | Oui<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>   | Oui<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>   | Oui<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>   | Oui<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>   | Oui<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>   | Oui<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>   | Oui<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>           | Oui<br/>    | VA<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>           | Oui<br/>    | VA<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ 3DES \_ Ede \_ CBC \_ SHA<br/>          | Oui<br/>    | VA<br/>         | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ RC4 \_ 128 \_ MD5<br/>                     | Non<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ avec \_ MD5<br/>                      | Non<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ avec \_ MD5<br/>           | Non<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS \_ RSA \_ avec \_ \_ MD5 null<br/>                         | Non<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ \_ SHA null<br/>                         | Non<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Les suites de chiffrement suivantes sont prises en charge par Schannel. Toutefois, ils ne sont pas présents par défaut. Ils doivent être ajoutés en fonction des besoins. Pour plus d’informations sur l’ajout de suites de chiffrement au fournisseur Schannel, consultez [hiérarchisation des suites de chiffrement Schannel](prioritizing-schannel-cipher-suites.md).

-   \_Exportation RSA \_ TLS \_ avec \_ RC4 \_ 40 \_ MD5
-   TLS \_ RSA \_ EXPORT1024 \_ avec \_ RC4 \_ 56 \_ SHA
-   TLS \_ RSA \_ EXPORT1024 \_ avec \_ des \_ CBC \_ SHA
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ des \_ 64 \_ CBC \_ avec \_ MD5
-   TLS \_ RSA \_ avec \_ des \_ CBC \_ SHA
-   TLS \_ RSA \_ avec \_ \_ MD5 null
-   TLS \_ RSA \_ avec \_ \_ SHA null
-   TLS \_ dhe \_ DSS \_ EXPORT1024 \_ avec \_ des \_ CBC \_ SHA
-   TLS \_ dhe \_ DSS \_ avec \_ des \_ CBC \_ SHA

**Windows Server 2003 et Windows XP :** Pour plus d’informations sur les suites de chiffrement prises en charge, consultez les rubriques suivantes.

| Rubrique                                                                         | Description                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Suites de chiffrement TLS](tls-cipher-suites.md)<br/>                         | informations sur les suites de chiffrement disponibles avec le protocole TLS dans Windows Server 2003 et Windows XP.<br/>              |
| [Protocole SSL (Secure Sockets Layer)](secure-sockets-layer-protocol.md)<br/> | informations générales sur les protocoles SSL 2,0 et 3,0, y compris les suites de chiffrement disponibles dans Windows Server 2003 et Windows XP.<br/> |



 

 

 
