---
description: Répertorie les modifications apportées aux fonctionnalités d’enveloppement des données.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Ajouts de données enveloppées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527844"
---
# <a name="enveloped-data-additions"></a>Ajouts de données enveloppées

Les modifications suivantes ont été apportées aux fonctionnalités de données enveloppées :

-   L’identification du destinataire peut être effectuée non seulement par l’émetteur et le numéro de série (PKCS \# 7 1,5), mais également par l’identificateur de clé.
-   Trois options d’échange de clés de destinataire sont fournies :
    -   Transport de clé à l’aide de clés RSA.
    -   Accord de clé à l’aide de Ephemeral-Static Diffie-Hellman les clés d’algorithme encapsulées avec 3DES ou RC2, ou Ephemeral-Static les clés d’algorithme Diffie-Hellman elliptique Curve encapsulées avec AES.
    -   Clé de chiffrement de clé ou transfert de clé de liste de messagerie où la clé utilisée pour chiffrer la clé de chiffrement de contenu a déjà été distribuée aux destinataires. RC2, 3DES et AES sont autorisés en tant qu’algorithmes de renvoi à la clé.
-   Les attributs non protégés peuvent être inclus dans le message.
-   Un champ **OriginatorInfo** contenant des informations sur l’expéditeur a été ajouté et peut contenir des certificats et des listes de révocation de certificats.
-   Les algorithmes basés sur le chiffrement à courbe elliptique (ECC) et AES requièrent Windows Vista ou une version ultérieure.

 

 



