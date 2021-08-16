---
description: Écriture de filtres de transformation
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Écriture de filtres de transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe8329809b6fe93ea33a9842f57733d7539a56e2ac21abfcf304d2ed780e6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816836"
---
# <a name="writing-transform-filters"></a>Écriture de filtres de transformation

Cette section décrit comment écrire un filtre de transformation, défini en tant que filtre avec une seule broche d’entrée et une seule broche de sortie. Pour illustrer les étapes, cette section décrit un filtre de transformation hypothétique qui produit une vidéo encodée en longueur d’exécution (RLE). Elle ne décrit pas l’algorithme d’encodage RLE proprement dit, mais uniquement les tâches spécifiques à DirectShow. (DirectShow fournit déjà un codec RLE par le biais du filtre de [compresseur AVI](avi-compressor-filter.md) .)

cette section part du principe que vous allez utiliser la bibliothèque de classes de base DirectShow pour créer des filtres. Bien que vous puissiez écrire un filtre sans celui-ci, la bibliothèque de classes de base est fortement recommandée.

> [!Note]  
> avant d’écrire un filtre de transformation, déterminez si un objet média DirectX (DMO) répondrait à vos besoins. DMOs peut faire beaucoup des mêmes choses que les filtres et le modèle de programmation pour DMOs est plus simple. les DMOs sont hébergés dans DirectShow via le filtre de [Wrapper DMO](dmo-wrapper-filter.md) , mais peuvent également être utilisés en dehors de DirectShow. Les DMOs sont désormais la solution recommandée pour les encodeurs et les décodeurs.

 

Cette section comprend les rubriques suivantes :

-   [Étape 1. Choisir une classe de base](step-1--choose-a-base-class.md)
-   [Étape 2. Déclarer la classe de filtre](step-2--declare-the-filter-class.md)
-   [Étape 3. Prendre en charge la négociation de type de média](step-3--support-media-type-negotiation.md)
-   [Étape 4. Définir les propriétés d’allocateur](step-4--set-allocator-properties.md)
-   [Étape 5. Transformer l’image](step-5--transform-the-image.md)
-   [Étape 6. Ajouter la prise en charge de COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[génération de filtres de DirectShow](building-directshow-filters.md)
</dt> <dt>

[DirectShow Classes de base](directshow-base-classes.md)
</dt> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



