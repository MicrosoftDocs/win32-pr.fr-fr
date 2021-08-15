---
description: Le tableau suivant répertorie les algorithmes pris en charge par le fournisseur de services de chiffrement Microsoft Advanced Encryption Standard (AES).
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: Algorithmes du fournisseur AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a06381c3f7fcf3d410a9a9a90c70633cab17c1ffd2e3e967ba6f3e7c3787fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773774"
---
# <a name="aes-provider-algorithms"></a>Algorithmes du fournisseur AES

Le tableau suivant répertorie les algorithmes pris en charge par le fournisseur de services de chiffrement Microsoft [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES).



| ID d’algorithme       | Description                                                                                                                                                     | Commentaires                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Longueur de clé : 168 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Aucun Salt n’est autorisé.<br/>                          |
| CALG \_ 3des \_ 112    | Chiffrement [*triple des*](../secgloss/t-gly.md) à deux clés.                                                            | Longueur de clé : 112 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Aucun Salt n’est autorisé.<br/>                          |
| CALG \_ AES \_ 128     | Algorithme de chiffrement par bloc AES.                                                                                                                                 | Longueur de clé : 128 bits.                                                                                                                                      |
| CALG \_ AES \_ 192     | Algorithme de chiffrement par bloc AES.                                                                                                                                 | Longueur de clé : 192 bits.                                                                                                                                      |
| CALG \_ AES \_ 256     | Algorithme de chiffrement par bloc AES.                                                                                                                                 | Longueur de clé : 256 bits.                                                                                                                                      |
| CALG \_ des          | Chiffrement DES.                                                                                                                                                 | Longueur de clé : 56 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Aucun Salt n’est autorisé.<br/>                           |
| CALG \_ HMAC         | Algorithme de hachage à clé MAC.                                                                                                                                       | Calcul HMAC.                                                                                                                                          |
| CALG \_ Mac          | Algorithme de hachage à clé [*code d’Authentification de message*](../secgloss/m-gly.md) (Mac). | Chiffrement par bloc MAC.                                                                                                                                          |
| CALG \_ MD2          | Algorithme de hachage MD2.                                                                                                                                          | Pour plus d’informations, consultez l' [*algorithme MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algorithme de hachage MD5.                                                                                                                                          | Pour plus d’informations, consultez [*algorithme MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algorithme de chiffrement par bloc RC2.                                                                                                                                 | Longueur de clé : 128 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Longueur du Salt : peut être définie.<br/>                  |
| CALG \_ RC4          | Algorithme de chiffrement de flux RC4.                                                                                                                                | Longueur de clé : 128 bits. Longueur du Salt : peut être définie.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | Algorithme d’échange de clés publiques RSA.                                                                                                                              | Longueur de clé : peut être défini, 384 bits à 16 384 bits par incréments de 8 bits. Longueur de clé par défaut : 1 024 bits.<br/>                                            |
| CALG \_ RSA \_ Sign    | Algorithme de signature de clé publique RSA.                                                                                                                             | Longueur de clé : peut être défini, 384 bits à 16 384 bits par incréments de 8 bits. Longueur de clé par défaut : 1 024 bits.<br/> La signature est conforme à PKCS \# 6.<br/> |
| CALG \_ SHA          | Algorithme de hachage SHA.                                                                                                                                          | Pour plus d’informations, consultez [*algorithme de hachage sécurisé*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Identique à **CALG \_ SHA**.                                                                                                                                          | Pour plus d’informations, consultez [*algorithme de hachage sécurisé*](../secgloss/s-gly.md).               |
| CALG \_ SHA \_ 256     | Algorithme de hachage SHA.                                                                                                                                          | Longueur de clé : 256 bits. **Windows XP :** Cet algorithme n’est pas pris en charge.<br/>                                                                           |
| CALG \_ SHA \_ 384     | Algorithme de hachage SHA.                                                                                                                                          | Longueur de clé : 384 bits. **Windows XP :** Cet algorithme n’est pas pris en charge.<br/>                                                                           |
| CALG \_ SHA \_ 512     | Algorithme de hachage SHA.                                                                                                                                          | Longueur de clé : 512 bits. **Windows XP :** Cet algorithme n’est pas pris en charge.<br/>                                                                           |
| CALG \_ SSL3 \_ SHAMD5 | Algorithme d’authentification du client SSL3.                                                                                                                           | Pour plus d’informations, consultez [création d’un \_ hachage CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
