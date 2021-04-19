---
description: Horloges de référence
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Horloges de référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b958787f4dbdb20cd595b10cf486f59222a072
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515739"
---
# <a name="reference-clocks"></a>Horloges de référence

L’une des fonctions du gestionnaire de graphique de filtre consiste à synchroniser tous les filtres du graphique avec la même horloge, appelée *horloge de référence*.

Tout objet qui expose l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) peut agir comme l’horloge de référence. L’horloge de référence peut être fournie par un filtre DirectShow, généralement le convertisseur audio, qui a accès à une horloge matérielle. En guise de solution de secours, le gestionnaire de graphes de filtres peut utiliser l’heure système.

De façon nominale, une horloge de référence mesure le temps en intervalles de 100 nanosecondes, bien que la précision réelle de l’horloge puisse être inférieure. Pour récupérer l’heure actuelle de l’horloge, appelez la méthode [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) . La ligne de base de l’horloge (l’heure à partir de laquelle elle commence le comptage) dépend de l’implémentation. par conséquent, la valeur retournée par **getTime** n’est pas fondamentalement significative. Ce qui importe est le Delta à partir duquel le graphique commence à s’exécuter.

Bien que la précision d’une horloge de référence puisse varier, il est garanti que les temps retournés par la méthode [**getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) augmentent de manière monotone. En d’autres termes, les temps d’horloge ne seront jamais redirigés vers l’arrière. Si une horloge de référence génère des temps d’horloge à partir d’une source matérielle et que l’horloge matérielle passe en arrière (par exemple, s’il y a un ajustement de l’horloge), la méthode **getTime** doit continuer à retourner la dernière heure signalée jusqu’à ce que l’horloge matérielle soit interceptée. Pour plus d’informations, consultez [**CBaseReferenceClock, classe**](cbasereferenceclock.md).

**Horloge de référence par défaut**

Le gestionnaire de graphes de filtres sélectionne automatiquement une horloge de référence lorsque le graphique s’exécute. Il utilise l’algorithme suivant pour sélectionner l’horloge :

-   Si l’application a sélectionné une horloge (voir ci-dessous), utilisez cette horloge.
-   Si le graphique contient un filtre de source dynamique qui prend en charge [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), utilisez ce filtre. Pour obtenir la définition d’une source dynamique, consultez la page [sources dynamiques](live-sources.md).
-   Si le graphique ne contient aucun filtre de source dynamique, utilisez un filtre dans le graphique qui prend en charge [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), en commençant par les convertisseurs et en amont. Préférer les filtres connectés aux filtres non connectés. (Si le graphique effectue le rendu d’un flux audio, cette étape de l’algorithme sélectionne normalement le filtre de convertisseur audio.)
-   Si aucun filtre ne fournit une horloge appropriée, utilisez l' [horloge de référence système](system-reference-clock.md), qui est basée sur l’heure système.

**Définition de l’horloge de référence**

Une application peut sélectionner une horloge en appelant la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) sur le gestionnaire de graphique de filtre. Vous ne devez effectuer cette opération que si vous avez une raison particulière de préférer une autre horloge.

Vous pouvez demander au gestionnaire de graphique de filtre de ne pas utiliser une horloge de référence en appelant [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) avec la valeur **null**. Par exemple, vous pouvez effectuer cette opération pour traiter les échantillons le plus rapidement possible. Pour restaurer l’horloge de référence par défaut, appelez la méthode [**IFilterGraph :: SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) sur le gestionnaire de graphique de filtre.

Chaque fois que l’horloge de référence change, le gestionnaire de graphique de filtre notifie chaque filtre en appelant sa méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) . Les applications ne doivent jamais appeler cette méthode sur les filtres.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de l’horloge du graphique](setting-the-graph-clock.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



