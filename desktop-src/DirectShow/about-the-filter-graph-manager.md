---
description: À propos du gestionnaire de graphique de filtre
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: À propos du gestionnaire de graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522239"
---
# <a name="about-the-filter-graph-manager"></a>À propos du gestionnaire de graphique de filtre

Le [Gestionnaire de graphes de filtres](filter-graph-manager.md) est un objet com qui contrôle les filtres dans un graphique de filtre. Il effectue de nombreuses fonctions, y compris les suivantes :

-   Coordination des changements d’état parmi les filtres.
-   Établissement d’une horloge de référence.
-   Communication des événements à l’application.
-   Fournir des méthodes pour que les applications génèrent le graphique de filtre.

Chacune de ces fonctions est décrite brièvement ici. Vous trouverez des détails ailleurs dans la documentation.

**Modifications d’État**. Les changements d’État dans les filtres doivent se produire dans un ordre particulier. Par conséquent, l’application n’émet pas de commandes de modification d’État directement aux filtres. Au lieu de cela, il fournit une seule commande au gestionnaire de graphique de filtre, qui distribue la commande à chacun des filtres. La recherche fonctionne de la même manière : l’application fournit une commande Seek au gestionnaire de graphique de filtre, qui le distribue aux filtres.

**Horloge de référence**. Tous les filtres du graphique utilisent la même horloge, appelée *horloge de référence*. L’horloge de référence garantit que tous les flux sont synchronisés. L’heure à laquelle un échantillon vidéo ou audio doit être rendu est l’heure de la *Présentation*. L’heure de la présentation est mesurée par rapport à l’horloge de référence. Le gestionnaire de graphe de filtre choisit une horloge de référence, généralement l’horloge de la carte son ou l’horloge système.

**Événements de graphique**. Le gestionnaire de graphique de filtre utilise une file d’attente d’événements pour informer l’application des événements qui se produisent dans le graphique de filtre. Ce mécanisme est similaire à une boucle de messages Windows.

**Méthodes de création de graphiques**. Le gestionnaire de graphes de filtre fournit des méthodes pour que l’application ajoute des filtres au graphique, connecte des filtres à d’autres filtres et déconnecte des filtres.

Une fonction que le gestionnaire de graphes de filtre ne gère pas consiste à déplacer les données d’un filtre à l’autre. Cela est effectué par les filtres eux-mêmes, par le biais de leurs connexions de code confidentiel. Le traitement se produit toujours sur un thread séparé.

> [!Note]  
> Les filtres sont toujours libres de thread, résident dans le même processus que le gestionnaire de graphes de filtre et sont chargés à partir de serveurs in-process. Par conséquent, les appels de méthode ne sont pas marshalés entre les filtres, ni entre les filtres et le gestionnaire de graphique de filtre.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Définition de l’horloge du graphique](setting-the-graph-clock.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



