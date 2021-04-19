---
description: Génération de graphiques dynamiques
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Génération de graphiques dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544549"
---
# <a name="dynamic-graph-building"></a>Génération de graphiques dynamiques

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

 

 



