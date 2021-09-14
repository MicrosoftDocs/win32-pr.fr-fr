---
description: Techniques d' Graph-Building générales
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Techniques d' Graph-Building générales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999143"
---
# <a name="general-graph-building-techniques"></a>Techniques d' Graph-Building générales

chaque DirectShow application commence par la création d’un graphique de filtre. à mesure que vous lisez les rubriques de vue d’ensemble de la documentation de DirectShow, vous constaterez que la plupart du début en décrivant le type de graphique de filtre dont vous avez besoin. Dans certains cas, il existe une méthode ou un objet d’assistance spécifiquement conçu pour créer ce type de graphique. par exemple, l’objet [dvd Graph Builder](dvd-graph-builder.md) crée des graphiques de lecture dvd. Dans d’autres cas, l’application doit construire le graphique en ajoutant des filtres et en les connectant.

Cette section présente des fonctions d’assistance qui implémentent des opérations de création de graphiques de base. elles peuvent être utilisées par n’importe quelle application DirectShow qui doit générer ou modifier un graphique de filtre. Cette section contient les rubriques suivantes :

-   [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md)
-   [Rechercher un code confidentiel non connecté sur un filtre](find-an-unconnected-pin-on-a-filter.md)
-   [Connecter Deux filtres](connect-two-filters.md)
-   [Rechercher une interface sur un filtre ou un code PIN](find-an-interface-on-a-filter-or-pin.md)
-   [Rechercher l’homologue d’un filtre](find-a-filters-peer.md)
-   [Supprimer tous les filtres dans le Graph](remove-all-the-filters-in-the-graph.md)
-   [création de graphiques avec le générateur de Graph de Capture](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[tâches de base DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Énumération des appareils et des filtres](enumerating-devices-and-filters.md)
</dt> <dt>

[Énumération d’objets dans un filtre Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Connecter intelligente](intelligent-connect.md)
</dt> </dl>

 

 



