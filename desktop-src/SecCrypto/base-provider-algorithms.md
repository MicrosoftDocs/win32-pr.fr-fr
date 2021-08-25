---
description: Le fournisseur de services de chiffrement de base Microsoft prend en charge les algorithmes suivants.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Algorithmes de fournisseur de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b6f3af49529ad46e70dd154c06febf433f5fb483861f7c0b2530af7ebbef2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879749"
---
# <a name="base-provider-algorithms"></a>Algorithmes de fournisseur de base

Le fournisseur de services de chiffrement de base Microsoft prend en charge les algorithmes suivants.



| ID d’algorithme                  | Description                                                                                                                                                               | Commentaires                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | Algorithme de hachage MD2<br/>                                                                                                                                          | Pour plus d’informations, consultez l' [*algorithme MD2*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ MD5<br/>          | Algorithme de hachage MD5<br/>                                                                                                                                          | Pour plus d’informations, consultez [*algorithme MD5*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ SHA<br/>          | Algorithme de hachage SHA<br/>                                                                                                                                          | Pour plus d’informations, consultez [*algorithme de hachage sécurisé*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ SHA1<br/>         | Identique à CALG \_ SHA<br/>                                                                                                                                              | Pour plus d’informations, consultez [*algorithme de hachage sécurisé*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ Mac<br/>          | Algorithme de hachage à clé (Mac) [*code d’Authentification de message*](../secgloss/m-gly.md)<br/> | Chiffrement par bloc MAC.<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | Algorithme de hachage à clé MAC<br/>                                                                                                                                       | Calcul HMAC.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | Algorithme d’authentification du client SLL3<br/>                                                                                                                           | Pour plus d’informations, consultez [création d’un \_ hachage CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                        |
| CALG \_ RSA \_ Sign<br/>    | Algorithme de signature de clé publique RSA<br/>                                                                                                                             | Longueur de clé : peut être défini de 384 bits à 16 384 bits par incréments de 8 bits.<br/> Longueur de clé par défaut : 512 bits.<br/> La signature est conforme à PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | Algorithme d’échange de clés publiques RSA<br/>                                                                                                                              | Longueur de clé : peut être défini de 384 bits à 1024 bits par incréments de 8 bits.<br/> Longueur de clé par défaut : 512 bits.<br/>                                              |
| CALG \_ RC2<br/>          | Algorithme de chiffrement par bloc RC2<br/>                                                                                                                                 | Longueur de clé : 40 bits.<br/> Mode par défaut : chaînage de blocs de chiffrement.<br/> Taille de bloc : 64 bits.<br/> Longueur du Salt : 88 bits.<br/>                        |
| CALG \_ RC4<br/>          | Algorithme de chiffrement de flux RC4<br/>                                                                                                                                | Longueur de clé : 40 bits.<br/> Longueur du Salt : 88 bits.<br/>                                                                                                        |
| CALG \_ des<br/>          | Chiffrement DES<br/>                                                                                                                                                 | Pour plus d’informations, voir [*Data Encryption Standard*](../secgloss/d-gly.md) (des).<br/>  |



 

 

 
