---
description: Les fonctions de message CryptoAPI adhèrent à la norme de la \# norme CMS (Cryptographic Message Syntax) PKCS 7. Les développeurs doivent être familiarisés avec cette spécification pour utiliser plus efficacement les fonctions de message de bas niveau. Quelques-unes de ses définitions sont mises en surbrillance ici.
ms.assetid: 99b633fe-9898-4570-ba8b-16ee78d351da
title: Concepts de syntaxe de la \# messagerie de chiffrement PKCS 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ead1c5e75737db80adbca725a30cb730b547be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536522"
---
# <a name="pkcs-7-cryptographic-messaging-syntax-concepts"></a>Concepts de syntaxe de la \# messagerie de chiffrement PKCS 7

Les fonctions de message CryptoAPI adhèrent à la norme de la [norme CMS (Cryptographic Message Syntax)](https://www.ietf.org/rfc/rfc3369.txt) [*PKCS \# 7*](../secgloss/p-gly.md) . Les développeurs doivent être familiarisés avec cette spécification pour utiliser plus efficacement les [*fonctions de message de bas niveau*](../secgloss/l-gly.md). Quelques-unes de ses définitions sont mises en surbrillance ici.

La \# norme PKCS 7 décrit une syntaxe générale pour les données auxquelles le [*chiffrement*](../secgloss/c-gly.md) peut être appliqué, telles que les [*signatures numériques*](../secgloss/d-gly.md) et les [*enveloppes numériques*](../secgloss/d-gly.md). La syntaxe admet la récursivité. ainsi, par exemple, une enveloppe peut être imbriquée dans une autre, ou une partie peut signer des données numériques qui ont déjà été placées dans une enveloppe. Il permet également d’authentifier les attributs arbitraires, tels que le délai de signature, en même temps que le contenu d’un message. En outre, elle permet d’associer d’autres attributs, tels que des contre- [*signatures*](../secgloss/c-gly.md), à une signature.

Le type de données contenu dans un \# message PKCS 7 est appelé son type de contenu. Il existe deux classes de types de contenu : base et amélioré.

-   Les types de contenu de base contiennent uniquement des données sans améliorations de chiffrement. Il n’existe actuellement qu’un seul type de contenu dans cette classe, le [*type de contenu de données*](../secgloss/d-gly.md).
-   Les [*types de contenu améliorés*](../secgloss/e-gly.md) contiennent des données d’un certain type (éventuellement chiffré) et d’autres améliorations de chiffrement (telles que les hachages ou les signatures).

Le contenu de la classe améliorée utilise l’encapsulation, ce qui donne lieu aux termes du [*contenu externe*](../secgloss/o-gly.md) (celui contenant les améliorations) et du [*contenu interne*](../secgloss/i-gly.md) (celui qui est amélioré). Par exemple, une classe améliorée peut contenir le [*type de contenu de données*](../secgloss/d-gly.md) (classe de base) qui a une signature incluse. Dans ce cas, le type de contenu de données est le *contenu interne* et la combinaison du type de contenu de données et de la signature forme le contenu externe.

Les types de contenu définis dans la \# norme PKCS 7 sont les suivants.



| Type de contenu              | Description                                                                                                                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Données                      | Chaîne d’octets (**octet**).                                                                                                                                                                                                                                                                                           |
| Données signées               | Contenu de tout type et [*hachages*](../secgloss/h-gly.md) de message chiffré ([*Digests*](../secgloss/m-gly.md)) du contenu pour zéro ou plusieurs signataires.                                                                           |
| Données enveloppées            | Contenu chiffré de tout type et clé de chiffrement de contenu chiffré pour un ou plusieurs destinataires. La combinaison de contenu chiffré et de clé de chiffrement de contenu chiffré pour un destinataire est une [*enveloppe numérique*](../secgloss/d-gly.md) pour ce destinataire. |
| Données signées et enveloppées | Contenu chiffré de tout type, clés de chiffrement de contenu chiffrées pour un ou plusieurs destinataires et résumés des messages chiffrés doublement pour un ou plusieurs signataires. Le double chiffrement est constitué d’un chiffrement avec la clé privée d’un signataire, suivi d’un chiffrement avec la clé de chiffrement de contenu.                     |
| Données résumées             | Contenu de tout type et [*hachage*](../secgloss/h-gly.md) de message (Digest) du contenu.                                                                                                                                                                                             |
| Données chiffrées            | Contenu chiffré de tout type. Contrairement au [*type de contenu*](../secgloss/d-gly.md)enveloppéd-Data, le type de contenu de données chiffrées n’a ni destinataire ni clé de chiffrement de contenu chiffré. Les clés sont supposées être gérées par d’autres moyens.               |



 

> [!Note]  
> Tout au long de la \# spécification PKCS 7, les termes « *condensé* » et « [*condensé*](../secgloss/d-gly.md) » font référence à la valeur produite par l’application d’un [*algorithme de hachage*](../secgloss/h-gly.md) aux données. Cette documentation utilise les termes [*hachage*](../secgloss/h-gly.md) et *haché* dans le même but. Par exemple, le type de données utilisé avec les [*fonctions de message de bas niveau*](../secgloss/l-gly.md) est appelé haché et non condensé. Dans le cadre de cette documentation, les deux ensembles de termes peuvent être utilisés indifféremment.

 

 

 
