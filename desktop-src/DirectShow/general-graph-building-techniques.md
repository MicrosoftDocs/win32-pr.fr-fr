---
description: Techniques d' Graph-Building générales
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Techniques d' Graph-Building générales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200663"
---
# <a name="general-graph-building-techniques"></a>Techniques d' Graph-Building générales

Chaque application DirectShow démarre en générant un graphique de filtre. À mesure que vous lisez les rubriques de vue d’ensemble de la documentation DirectShow, vous constaterez que la plupart commencent par décrire le type de graphique de filtre dont vous avez besoin. Dans certains cas, il existe une méthode ou un objet d’assistance spécifiquement conçu pour créer ce type de graphique. Par exemple, l’objet [DVD Graph Builder](dvd-graph-builder.md) crée des graphiques de lecture DVD. Dans d’autres cas, l’application doit construire le graphique en ajoutant des filtres et en les connectant.

Cette section présente des fonctions d’assistance qui implémentent des opérations de création de graphiques de base. Elles peuvent être utilisées par n’importe quelle application DirectShow qui doit générer ou modifier un graphique de filtre. Cette section contient les rubriques suivantes :

-   [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md)
-   [Rechercher un code confidentiel non connecté sur un filtre](find-an-unconnected-pin-on-a-filter.md)
-   [Connecter deux filtres](connect-two-filters.md)
-   [Rechercher une interface sur un filtre ou un code PIN](find-an-interface-on-a-filter-or-pin.md)
-   [Rechercher l’homologue d’un filtre](find-a-filters-peer.md)
-   [Supprimer tous les filtres dans le graphique](remove-all-the-filters-in-the-graph.md)
-   [Création de graphiques à l’aide du générateur de graphiques de capture](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de base de DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Énumération des appareils et des filtres](enumerating-devices-and-filters.md)
</dt> <dt>

[Énumération d’objets dans un graphique de filtre](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Connexion intelligente](intelligent-connect.md)
</dt> </dl>

 

 



