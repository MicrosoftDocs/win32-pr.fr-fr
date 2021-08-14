---
description: Le fournisseur de services de chiffrement amélioré Microsoft prend en charge les algorithmes suivants.
ms.assetid: d58bcd99-c54b-4fda-9fe1-e10a66707d81
title: Algorithmes de fournisseur améliorés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a8be464a57a482fa74fef07de097508508d7e965a5c20817ccbd884bb169e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766100"
---
# <a name="enhanced-provider-algorithms"></a>Algorithmes de fournisseur améliorés

Le [fournisseur de services de chiffrement amélioré Microsoft](microsoft-enhanced-cryptographic-provider.md) prend en charge les algorithmes suivants.



| ID d’algorithme       | Description                                                                                                                                                     | Commentaires                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Longueur de clé : 168 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Aucun Salt n’est autorisé.<br/>                           |
| CALG \_ 3des \_ 112    | Chiffrement [*triple des*](../secgloss/t-gly.md) à deux clés.                                                            | Longueur de clé : 112 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Aucun Salt n’est autorisé.<br/>                           |
| CALG \_ des          | Chiffrement DES.                                                                                                                                                 | Longueur de clé : 56 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Aucun Salt n’est autorisé.<br/>                            |
| CALG \_ HMAC         | Algorithme de hachage à clé MAC.                                                                                                                                       | Calcul HMAC.                                                                                                                                          |
| CALG \_ Mac          | Algorithme de hachage à clé [*code d’Authentification de message*](../secgloss/m-gly.md) (Mac). | Chiffrement par bloc MAC.                                                                                                                                          |
| CALG \_ MD2          | Algorithme de hachage MD2.                                                                                                                                          | Pour plus d’informations, consultez l' [*algorithme MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algorithme de hachage MD5.                                                                                                                                          | Pour plus d’informations, consultez [*algorithme MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algorithme de chiffrement par bloc RC2.                                                                                                                                 | Longueur de clé : 128 bits. Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Longueur du Salt : peut être définie.<br/>                   |
| CALG \_ RC4          | Algorithme de chiffrement de flux RC4.                                                                                                                                | Longueur de clé : 128 bits. Longueur du Salt : peut être définie.<br/>                                                                                                   |
| CALG \_ RSA \_ KEYX    | Algorithme d’échange de clés publiques RSA.                                                                                                                              | Longueur de clé : peut être défini, 384 bits à 16 384 bits par incréments de 8 bits. Longueur de clé par défaut : 1 024 bits.<br/>                                            |
| CALG \_ RSA \_ Sign    | Algorithme de signature de clé publique RSA.                                                                                                                             | Longueur de clé : peut être défini, 384 bits à 16 384 bits par incréments de 8 bits. Longueur de clé par défaut : 1 024 bits.<br/> La signature est conforme à PKCS \# 6.<br/> |
| CALG \_ SHA          | Algorithme de hachage SHA.                                                                                                                                          | Pour plus d’informations, consultez [*algorithme de hachage sécurisé*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Identique à CALG \_ Sha.                                                                                                                                              | Pour plus d’informations, consultez [*algorithme de hachage sécurisé*](../secgloss/s-gly.md).               |
| CALG \_ SSL3 \_ SHAMD5 | Algorithme d’authentification du client SSL3.                                                                                                                           | Pour plus d’informations, consultez [création d’un \_ hachage CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
