---
description: Les algorithmes peuvent être pris en charge par le fournisseur de services de chiffrement Microsoft RSA/Schannel.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algorithmes de fournisseur RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dd7f22e6353544690c14091d29af50fec94dc3b65d6733aefc2a9fa8387bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900510"
---
# <a name="rsaschannel-provider-algorithms"></a>Algorithmes de fournisseur RSA/Schannel

Les algorithmes suivants peuvent être pris en charge par le fournisseur de services de chiffrement Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) .



| ID d’algorithme    | Description                                                                                                                         | Commentaires                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ RSA \_ KEYX | [ *Algorithme d’échange de clés* publiques RSA](../secgloss/k-gly.md) | Longueur de clé : peut être définie, 384 bits à 16 384 bits par incréments de 8 bits. Longueur de clé par défaut : 1 024 bits.<br/> |
| CALG \_ MD5       | Algorithme de hachage MD5.                                                                                                              | Fourni uniquement pour le hachage.                                                                                      |
| CALG \_ SHA       | Algorithme de hachage SHA.                                                                                                              | Doit être utilisé pour les signatures DSS.                                                                                |
| CALG \_ RC2       | Algorithme de chiffrement par bloc RC2.                                                                                                     | Longueur de clé : 40 à 88 bits                                                                                       |
| CALG \_ RC4       | Algorithme de chiffrement de flux RC4.                                                                                                    | Longueur de clé : 40 à 88 bits                                                                                       |



 

 

 
