---
description: Flow de données pour les développeurs de filtres
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Flow de données pour les développeurs de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ced9507856d7a6b8aea2acaea86c20b393b8d937ab4427bf522596a29ba690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749369"
---
# <a name="data-flow-for-filter-developers"></a>Flow de données pour les développeurs de filtres

Cette section décrit en détail la façon dont les données se déplacent dans le graphique de filtre. Il se concentre sur le transport de mémoire local à l’aide de l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ou [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Elle est destinée aux développeurs qui écrivent leurs propres filtres personnalisés. pour obtenir une présentation générale de la façon dont Microsoft DirectShow gère le workflow de données, consultez [Flow de données dans le Graph de filtre](data-flow-in-the-filter-graph.md).

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

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



