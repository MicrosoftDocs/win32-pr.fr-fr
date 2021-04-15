---
description: Pour utiliser des certificats pour la sécurité, l’authenticité et la validité de chaque certificat reçu doivent être vérifiées. Cette vérification dépend du concept de confiance et de la délégation du \[ Kit de développement logiciel (SDK) de la plateforme de confiance \] .
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Chaînes de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea42b6788997a86aade6f89d0f35d92a74daafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484689"
---
# <a name="certificate-chains"></a>Chaînes de certificats

Pour utiliser des [*certificats*](../secgloss/c-gly.md) pour la sécurité, l’authenticité et la validité de chaque certificat reçu doivent être vérifiées. Cette vérification dépend du concept de confiance et de la délégation de confiance ; Pour plus d’informations, consultez [hiérarchie d’approbation](hierarchy-of-trust.md).

Chaque certificat contient un champ objet qui identifie la personne ou le groupe pour lequel le certificat a été émis. Chaque certificat contient également un champ d’émetteur qui identifie l' [*autorité de certification*](../secgloss/c-gly.md) habilitée à certifier l’identité du sujet.

Une chaîne de certificats se compose de tous les certificats nécessaires pour certifier le sujet identifié par le certificat de fin. Dans la pratique, cela comprend le certificat de fin, les certificats des autorités de certification intermédiaires et le certificat d’une autorité de certification racine approuvée par toutes les parties de la chaîne. Chaque autorité de certification intermédiaire de la chaîne contient un certificat émis par l’autorité de certification un niveau au-dessus de lui dans la hiérarchie d’approbation. L’autorité de certification racine émet un certificat pour elle-même.

Le processus de vérification de l’authenticité et de la validité d’un certificat nouvellement reçu implique la vérification de tous les certificats de la chaîne de certificats à partir de l’autorité de certification d’origine, approuvée de manière universelle, par le biais de toutes les autorités de certification intermédiaires, jusqu’au certificat que vous venez de recevoir, appelé certificat final. Un nouveau certificat peut être approuvé uniquement si chaque certificat de la chaîne de ce certificat est correctement émis et valide.

Le suivi de tous les certificats qui reviennent à un nouveau certificat de fin peut devenir fastidieux. Par conséquent, la technologie [*CryptoAPI*](../secgloss/c-gly.md) 2,0 fournit des fonctions qui automatisent la création de la chaîne de certificats qui renvoie un certificat de fin donné. Ces fonctions vérifient et signalent également la validité de chaque certificat dans une chaîne.

Les fonctions de création de chaîne et de vérification de [*CryptoAPI*](../secgloss/c-gly.md) 2,0 utilisent un moteur de chaîne pour créer et vérifier des chaînes de certificats. Un moteur de chaîne définit un espace de noms de magasin et le partitionnement de cache pour l’infrastructure de chaînage de certificats. CryptoAPI 2.0 fournit un moteur de chaîne par défaut pour tout processus d’application qui utilise uniquement les magasins système par défaut (par exemple, MY, root, CA et Trust) pour la création et la mise en cache de chaînes. Une application peut définir son propre espace de noms de magasin ou avoir son propre cache partitionné en créant son propre moteur de chaîne. Pour obtenir un comportement de mise en cache optimal, nous vous recommandons de créer un moteur de chaîne unique au démarrage de l’application et d’utiliser ce moteur de chaîne pendant toute la durée de vie de l’application.

Pour obtenir la liste des fonctions, consultez fonctions de vérification de la [chaîne de certificats](cryptography-functions.md). Pour un programme qui crée des chaînes de certificats et vérifie les certificats, consultez [exemple de programme C : création d’une chaîne de certificats](example-c-program-creating-a-certificate-chain.md).

 

 
