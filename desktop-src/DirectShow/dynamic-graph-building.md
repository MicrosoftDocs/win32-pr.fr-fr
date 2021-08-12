---
description: génération de Graph dynamique
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: génération de Graph dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c7296b95bc97461eb5a16ee577acb4bd267ee1a25f9be357a00fef7d4bdba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652789"
---
# <a name="dynamic-graph-building"></a>génération de Graph dynamique

Si vous avez besoin de modifier un graphique de filtre existant, vous pouvez arrêter le graphique, apporter les modifications et redémarrer le graphique. Il s’agit généralement de la meilleure approche. Toutefois, dans certaines circonstances, vous souhaiterez peut-être modifier un graphique pendant qu’il est toujours en cours d’exécution. Par exemple :

-   L’application insère un filtre d’effets vidéo pendant la lecture.
-   Un filtre source change de type de média pendant, ce qui peut nécessiter un nouveau filtre de décompression.
-   L’application ajoute un nouveau flux vidéo au graphique.

Il s’agit de tous les exemples de *création de graphique dynamique*, terme qui couvre tout type de modification apportée à un graphique de filtre pendant que le graphique continue à s’exécuter. La génération de graphiques dynamiques peut être lancée par une application ou par un filtre dans le graphique. Trois scénarios distincts sont possibles :

-   [Modifications de format dynamique](dynamic-format-changes.md): un filtre peut changer les formats pendant, sans qu’il soit nécessaire de supprimer ou de remplacer des filtres.
-   [Reconnexion dynamique](dynamic-reconnection.md): modification du graphique en ajoutant ou en supprimant des filtres.
-   [Chaînes de filtre](filter-chains.md): ajout, suppression et contrôle des chaînes de filtres.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de DirectShow](about-directshow.md)
</dt> </dl>

 

 



