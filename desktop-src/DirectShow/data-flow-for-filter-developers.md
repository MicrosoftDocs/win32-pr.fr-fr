---
description: Transmission de données pour les développeurs de filtres
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Transmission de données pour les développeurs de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033550"
---
# <a name="data-flow-for-filter-developers"></a>Transmission de données pour les développeurs de filtres

Cette section décrit en détail la façon dont les données se déplacent dans le graphique de filtre. Il se concentre sur le transport de mémoire local à l’aide de l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ou [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Elle est destinée aux développeurs qui écrivent leurs propres filtres personnalisés. Pour obtenir une présentation générale de la façon dont Microsoft DirectShow gère le workflow de données, consultez [Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md).

Un grand nombre de données se déplacent dans un graphique de filtre. Il se divise en deux catégories : données de média et données de contrôle. En général, les données multimédia transitent en aval et contrôlent les flux de données en amont. Les données multimédias incluent les images vidéo, les échantillons audio, les paquets MPEG, etc. qui composent un flux, mais également les commandes de vidage, les notifications de fin de flux et les autres données qui transitent par le flux. Les données de contrôle ne font pas partie du flux multimédia. Les requêtes de contrôle qualité et les commandes de recherche sont des exemples de données de contrôle.

Cette section contient les articles suivants.

-   [Exemples de livrables](delivering-samples.md)
-   [Traitement des données](processing-data.md)
-   [Notifications de fin de flux](end-of-stream-notifications.md)
-   [Nouveaux segments](new-segments.md)
-   [Vidage](flushing.md)
-   [Cherche](seeking.md)
-   [Modifications de format dynamique](dynamic-format-changes.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion du contrôle de la qualité](quality-control-management.md)
</dt> <dt>

[Threads et sections critiques](threads-and-critical-sections.md)
</dt> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



