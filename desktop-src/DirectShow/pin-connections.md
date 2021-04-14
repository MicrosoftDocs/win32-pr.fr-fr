---
description: Épingler les connexions
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Épingler les connexions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b509abddf4a915b65dfd322f76b4afb132a7f835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392507"
---
# <a name="pin-connections"></a>Épingler les connexions

Les filtres se connectent à leurs codes confidentiels, via l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) . Les broches de sortie se connectent aux broches d’entrée. Chaque connexion de code confidentiel a un type de support, décrit par la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Une application connecte les filtres en appelant des méthodes sur le gestionnaire de graphique de filtre, jamais en appelant des méthodes sur les filtres ou les épingles eux-mêmes. L’application peut spécifier directement les filtres à connecter, en appelant la méthode [**IFilterGraph :: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) ou [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) . elle peut aussi connecter indirectement des filtres, à l’aide d’une méthode de création de graphiques telle que [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).

Pour que la connexion aboutisse, les deux filtres doivent se trouver dans le graphique de filtre. L’application peut ajouter un filtre au graphique en appelant la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Le gestionnaire de graphes de filtre peut également ajouter des filtres au graphique. Lorsqu’un filtre est ajouté, le gestionnaire de graphes de filtre appelle la méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) du filtre pour notifier le filtre.

La structure générale du processus de connexion est la suivante :

1.  Le gestionnaire de graphique de filtre appelle [**IPIN :: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) sur la broche de sortie, en passant un pointeur vers la broche d’entrée.
2.  Si la broche de sortie accepte la connexion, elle appelle [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sur la broche d’entrée.
3.  Si la broche d’entrée accepte également la connexion, la tentative de connexion a échoué et les broches sont connectées.

Certaines broches peuvent être déconnectées et reconnectées pendant que le filtre est actif. Ce type de reconnexion est appelé reconnexion *dynamique* . Pour plus d’informations, consultez [génération de graphiques dynamiques](dynamic-graph-building.md). Toutefois, la plupart des filtres ne prennent pas en charge la reconnexion dynamique.

Les filtres sont généralement connectés dans l’ordre en aval (en d’autres termes, les broches d’entrée du filtre sont connectées avant les broches de sortie). Un filtre doit toujours prendre en charge cet ordre de connexion. Certains filtres prennent également en charge les connexions dans l’ordre inverse, en commençant par les broches de sortie, suivies des broches d’entrée. Par exemple, il peut être possible de connecter la broche de sortie d’un filtre MULTIPLEXeur au filtre d’écriture de fichier, avant de connecter les broches d’entrée du filtre MUX.

Quand la méthode **Connect** ou **ReceiveConnection** d’un pin est appelée, le code confidentiel doit vérifier qu’il peut prendre en charge la connexion. Les détails dépendent du filtre concerné. Les tâches les plus courantes sont les suivantes :

-   Vérifier que le type de support est acceptable
-   Négocier un allocateur
-   Interrogez l’autre code PIN pour les interfaces requises.

 

 



