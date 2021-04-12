---
description: Considérations relatives aux performances (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Considérations relatives aux performances (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033631"
---
# <a name="performance-considerations-direct3d-10"></a>Considérations relatives aux performances (Direct3D 10)

## <a name="using-effect-pools"></a>Utilisation des pools d’effets

Il est courant que les pipelines de rendu utilisent de nombreux nuanceurs pour afficher différents types d’objets et effets spéciaux. Le nuanceur est un mélange d’États qui sont communs à tous les nuanceurs tels qu’une matrice universelle ou une position légère, et d’autres États spécifiques à chaque nuanceur, tels que la couleur diffuse d’un objet ou le calcul de surbrillance spéculaire. Un pool d’effets est un emplacement en mémoire où stocker l’État utilisé dans de nombreux nuanceurs, ainsi que des objets d’appareil courants tels que les nuanceurs, les objets d’état de rendu et les mémoires tampons constantes. L’amélioration des performances résulte de la mise à jour de l’État commun une seule fois pour tous les nuanceurs qui ont besoin de cet État.

Un pool d’effets est un emplacement de mémoire partagée pour l’état de l’effet. Un pool est créé de la même façon qu’un effet ; Il peut être créé à partir de la mémoire (ou d’un fichier ou d’une ressource). Cela entraîne deux types différents d’effets : un effet global qui ne dépend pas de l’état d’un autre effet par rapport à un effet enfant qui dépend de l’état d’un autre effet.

Vous spécifiez si un effet est un effet global (cas par défaut) ou un effet enfant (en fournissant l’effet D3D10 l’indicateur de compilation d’effet [ \_ \_ \_ enfant \_ ](d3d10-effect.md) ) lors de la création de l’effet. Un effet global peut servir de pool d’effets ; un effet enfant ne peut pas être un pool d’effets.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un effet](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[Effets (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



