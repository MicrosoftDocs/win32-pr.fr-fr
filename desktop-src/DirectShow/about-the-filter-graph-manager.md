---
description: à propos du gestionnaire de Graph de filtre
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: à propos du gestionnaire de Graph de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112402"
---
# <a name="about-the-filter-graph-manager"></a>à propos du gestionnaire de Graph de filtre

le [gestionnaire de Graph de filtre](filter-graph-manager.md) est un objet COM qui contrôle les filtres dans un graphique de filtre. Il effectue de nombreuses fonctions, y compris les suivantes :

-   Coordination des changements d’état parmi les filtres.
-   Établissement d’une horloge de référence.
-   Communication des événements à l’application.
-   Fournir des méthodes pour que les applications génèrent le graphique de filtre.

Chacune de ces fonctions est décrite brièvement ici. Vous trouverez des détails ailleurs dans la documentation.

**Modifications d’État**. Les changements d’État dans les filtres doivent se produire dans un ordre particulier. Par conséquent, l’application n’émet pas de commandes de modification d’État directement aux filtres. au lieu de cela, il fournit une commande unique au gestionnaire de Graph de filtre, qui distribue la commande à chacun des filtres. la recherche fonctionne de la même manière : l’application fournit une commande seek au gestionnaire de Graph de filtre, qui le distribue aux filtres.

**Horloge de référence**. Tous les filtres du graphique utilisent la même horloge, appelée *horloge de référence*. L’horloge de référence garantit que tous les flux sont synchronisés. L’heure à laquelle un échantillon vidéo ou audio doit être rendu est l’heure de la *Présentation*. L’heure de la présentation est mesurée par rapport à l’horloge de référence. le gestionnaire de Graph de filtre choisit une horloge de référence, généralement l’horloge de la carte son ou l’horloge système.

**événements de Graph**. le gestionnaire de Graph de filtre utilise une file d’attente d’événements pour informer l’application des événements qui se produisent dans le graphique de filtre. ce mécanisme est similaire à une boucle de messages Windows.

**méthodes de création de Graph**. le gestionnaire de Graph de filtre fournit des méthodes pour que l’application ajoute des filtres au graphique, connecte des filtres à d’autres filtres et déconnecte les filtres.

une fonction que le gestionnaire de Graph de filtre ne gère pas consiste à déplacer les données d’un filtre à l’autre. Cela est effectué par les filtres eux-mêmes, par le biais de leurs connexions de code confidentiel. Le traitement se produit toujours sur un thread séparé.

> [!Note]  
> les filtres sont toujours à thread libre, résident dans le même processus que le gestionnaire de Graph de filtre et sont chargés à partir des serveurs in-process. par conséquent, les appels de méthode ne sont pas marshalés entre les filtres, ni entre les filtres et le gestionnaire de Graph de filtre.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[données Flow dans le filtre Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[définition de l’horloge de Graph](setting-the-graph-clock.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



