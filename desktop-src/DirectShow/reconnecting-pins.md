---
description: Reconnexion des broches
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: Reconnexion des broches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8bb214307a5c17639d98ae07284abddca4d5beb11b966150d8b7ec46013853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072773"
---
# <a name="reconnecting-pins"></a>Reconnexion des broches

Pendant une connexion de code confidentiel, un filtre peut se déconnecter et reconnecter l’un de ses autres broches, comme suit :

1.  Le filtre appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur le code confidentiel de l’autre filtre et spécifie le nouveau type de média.
2.  Si **QueryAccept** retourne S \_ OK, le filtre appelle [**IFilterGraph2 :: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) pour reconnecter les broches.

Voici quelques exemples de cas où un filtre peut avoir besoin de reconnecter des broches :

-   **Filtres tee.** Un *filtre tee* fractionne un flux d’entrée en plusieurs sorties sans modifier les données dans le flux. Un filtre tee peut accepter une plage de types de médias, mais les types doivent correspondre sur toutes les connexions de code confidentiel. Par conséquent, lorsque la broche d’entrée se connecte, il se peut que le filtre doive renégocier toutes les connexions existantes sur les broches de sortie, et vice versa. Pour obtenir un exemple, consultez l' [exemple de filtre InfTee](inftee-filter-sample.md).
-   **Filtres de transfert en place.** Un filtre *de transfert sur place* modifie les données d’entrée dans la mémoire tampon d’origine au lieu de copier les données dans une mémoire tampon de sortie distincte. Un filtre de transfert sur place doit utiliser le même allocateur pour les connexions en amont et en aval. Le premier code PIN pour la connexion (entrée ou sortie) négocie une allocation de la manière habituelle. Toutefois, lorsque l’autre code pin se connecte, le premier allocateur peut ne pas être acceptable. Dans ce cas, la deuxième broche choisit un allocateur différent et le premier code confidentiel se reconnecte à l’aide du nouvel allocateur. Pour obtenir un exemple d’implémentation, consultez la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

dans la méthode **ReconnectEx** , le gestionnaire de Graph de filtre se déconnecte de façon asynchrone et reconnecte les broches. Le filtre ne doit pas tenter la reconnexion à moins que **QueryAccept** retourne la valeur S \_ OK. Dans le cas contraire, le code PIN restera déconnecté, provoquant des erreurs de graphique. en outre, le filtre doit demander la reconnexion à l’intérieur de la méthode [**IPin :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , sur le même thread. si la méthode **Connecter** retourne sur un thread, alors qu’un autre thread effectue la demande de reconnexion, le gestionnaire de Graph de filtre peut exécuter le graphique avant de procéder à la reconnexion, ce qui entraîne des erreurs de graphique.

 

 



