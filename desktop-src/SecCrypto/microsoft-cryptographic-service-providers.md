---
description: Répertorie les fournisseurs de services de chiffrement disponibles auprès de Microsoft.
ms.assetid: 1461914e-5506-4f24-97da-3d2148aafd1c
title: Fournisseurs de services de chiffrement Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 294d00660cbfa89c6113e6e9fcf2600b2f745e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513437"
---
# <a name="microsoft-cryptographic-service-providers"></a>Fournisseurs de services de chiffrement Microsoft

Les [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) suivants sont actuellement disponibles auprès de Microsoft.



| Fournisseur                                                                                                                                 | Description                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fournisseur de services de chiffrement de base Microsoft](microsoft-base-cryptographic-provider.md)                                                       | Vaste ensemble de fonctionnalités de chiffrement de base pouvant être exportées vers d’autres pays ou régions.                                                                                                                                                     |
| [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md)                                                   | Extension du fournisseur de services de chiffrement de base Microsoft disponible avec Windows XP et versions ultérieures.                                                                                                                                                           |
| [Fournisseur de services de chiffrement amélioré Microsoft](microsoft-enhanced-cryptographic-provider.md)                                               | Fournisseur de chiffrement de base Microsoft avec les clés et les algorithmes plus longs.                                                                                                                                                                |
| [Fournisseur de services de chiffrement AES Microsoft](microsoft-aes-cryptographic-provider.md)                                                         | Fournisseur de services de chiffrement amélioré Microsoft avec prise en charge des algorithmes de chiffrement AES.                                                                                                                                                                    |
| [Fournisseur de services de chiffrement DSS Microsoft](microsoft-dss-cryptographic-provider.md)                                                         | Fournit des fonctionnalités de hachage, de signature de données et de vérification de signature à l’aide des algorithmes [*SHA*](../secgloss/s-gly.md)(Secure Hash Algorithm) et DSS (Digital Signature standard). |
| [Microsoft Base DSS et Diffie-Hellman fournisseur de services de chiffrement](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)         | Sur-ensemble du fournisseur de services de chiffrement DSS qui prend également en charge Diffie-Hellman l’échange de clés, le hachage, la signature des données et la vérification de signature à l’aide des algorithmes SHA (Secure Hash Algorithm) et DSS (Digital Signature standard).                    |
| [Microsoft Enhanced DSS et Diffie-Hellman fournisseur de services de chiffrement](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md) | Prend en charge l’échange de clés Diffie-Hellman (un dérivé de 40 bits), le hachage SHA, la signature des données DSS et la vérification de la signature DSS.                                                                                                                           |
| [Fournisseur de services de chiffrement Microsoft DSS et Diffie-Hellman/Schannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md) | Prend en charge le hachage, la signature des données avec DSS, la génération de clés de Diffie-Hellman (D-H), l’échange de clés D-H et l’exportation d’une clé D-H. Ce CSP prend en charge la dérivation de clés pour les protocoles SSL3 et TLS1.                                                           |
| [Fournisseur de services de chiffrement Microsoft RSA/Schannel](microsoft-rsa-schannel-cryptographic-provider.md)                                       | Prend en charge le hachage, la signature des données et la vérification de signature. L’identificateur d’algorithme CALG \_ SSL3 \_ SHAMD5 est utilisé pour l’authentification du client SSL 3,0 et TLS 1,0. Ce CSP prend en charge la dérivation de clés pour les protocoles SSL2, PCT1, SSL3 et TLS1.             |
| [Fournisseur de chiffrement de signature Microsoft RSA](microsoft-rsa-signature-cryptographic-provider.md)                                     | Assure la signature des données et la vérification de la signature.                                                                                                                                                                                                        |



 

 

 
