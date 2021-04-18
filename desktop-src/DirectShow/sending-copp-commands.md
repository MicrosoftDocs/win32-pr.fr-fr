---
description: Envoi de commandes COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Envoi de commandes COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516340"
---
# <a name="sending-copp-commands"></a>Envoi de commandes COPP

Pour envoyer une commande COPP (Certified Output Protection Protocol), remplissez une structure [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) comme suit :

-   **guidCommandID**. GUID qui identifie la commande. Consultez les informations de référence sur les commandes COPP.
-   **dwSequence**. Numéro de séquence de la commande. Incrémentez cette valeur après chaque commande. (Cette valeur est indiquée en tant que **uCommandSeq** dans [le lancement d’une session Copp](initiating-a-copp-session.md).)
-   **cbSizeData**. Taille, en octets, des données nécessaires pour la commande.
-   **CommandData**. Données pour la commande.

Une fois que vous avez rempli ces données, calculez le MAC pour la commande :

1.  Calculez la balise OMAC-1 pour le bloc de données qui apparaît après le membre **macKDI** de la structure **AMCOPPCommand** .
2.  Copiez cette valeur dans le membre **macKDI** de la structure.

À présent, transmettez la structure à la méthode [**IAMCertifiedOutputProtection ::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



