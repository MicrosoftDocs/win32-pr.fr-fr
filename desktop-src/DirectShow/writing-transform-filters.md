---
description: Écriture de filtres de transformation
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Écriture de filtres de transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952185"
---
# <a name="writing-transform-filters"></a>Écriture de filtres de transformation

Cette section décrit comment écrire un filtre de transformation, défini en tant que filtre avec une seule broche d’entrée et une seule broche de sortie. Pour illustrer les étapes, cette section décrit un filtre de transformation hypothétique qui produit une vidéo encodée en longueur d’exécution (RLE). Elle ne décrit pas l’algorithme d’encodage RLE proprement dit, mais uniquement les tâches qui sont spécifiques à DirectShow. (DirectShow fournit déjà un codec RLE par le biais du filtre de [compresseur AVI](avi-compressor-filter.md) .)

Cette section part du principe que vous allez utiliser la bibliothèque de classes de base DirectShow pour créer des filtres. Bien que vous puissiez écrire un filtre sans celui-ci, la bibliothèque de classes de base est fortement recommandée.

> [!Note]  
> Avant d’écrire un filtre de transformation, déterminez si un objet multimédia DirectX (DMO) répondra à vos besoins. DMOs peut faire beaucoup des mêmes choses que les filtres et le modèle de programmation pour DMOs est plus simple. Les DMOs sont hébergés dans DirectShow via le filtre de [Wrapper DMO](dmo-wrapper-filter.md) , mais peuvent également être utilisés en dehors de DirectShow. Les DMOs sont désormais la solution recommandée pour les encodeurs et les décodeurs.

 

Cette section comprend les rubriques suivantes :

-   [Étape 1. Choisir une classe de base](step-1--choose-a-base-class.md)
-   [Étape 2. Déclarer la classe de filtre](step-2--declare-the-filter-class.md)
-   [Étape 3. Prendre en charge la négociation de type de média](step-3--support-media-type-negotiation.md)
-   [Étape 4. Définir les propriétés d’allocateur](step-4--set-allocator-properties.md)
-   [Étape 5. Transformer l’image](step-5--transform-the-image.md)
-   [Étape 6. Ajouter la prise en charge de COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération de filtres DirectShow](building-directshow-filters.md)
</dt> <dt>

[Classes de base DirectShow](directshow-base-classes.md)
</dt> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



