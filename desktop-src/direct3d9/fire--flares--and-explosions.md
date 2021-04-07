---
description: Vous pouvez utiliser Microsoft Direct3D pour simuler des phénomènes naturels impliquant des versions d’énergie.
ms.assetid: a16af13d-3a38-42b5-900b-ff58a0c917b2
title: Incendie, halos et explosions (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708730bd8e5f198664bb20c11fa98243ac98f0d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745565"
---
# <a name="fire-flares-and-explosions-direct3d-9"></a>Incendie, halos et explosions (Direct3D 9)

Vous pouvez utiliser Microsoft Direct3D pour simuler des phénomènes naturels impliquant des versions d’énergie. Par exemple, une application peut générer l’apparence d’un incendie en appliquant des textures de type flamme à un ensemble de panneaux. Cela est particulièrement efficace si l’application utilise une séquence de textures d’incendie pour animer la flamme sur chaque panneau de l’incendie. La variation de la vitesse de la lecture de l’animation du panneau d’affichage vers le panneau d’affichage augmente l’apparence des flammes réelles. Le semblance de la flamme 3D mélangée peut être obtenu en superposition des panneaux et des textures sur les panneaux.

Vous pouvez simuler des halos et des clignotements en appliquant des cartes de lumière plus lumineuses à toutes les primitives d’une scène. Bien qu’il s’agisse d’une technique de calcul à forte surcharge, elle permet à votre application de simuler un halo ou un flash localisé. Autrement dit, la partie de la scène d’où provient le halo ou le flash peut s’éclaircir en premier.

Une autre technique consiste à positionner un panneau avant la scène afin que l’intégralité de la zone de rendu cible soit couverte. L’application applique successivement les textures blanches aux panneaux et réduit la transparence dans le temps. L’intégralité de la scène est déplacée en blanc au moment où le temps passe. Il s’agit d’une méthode de faible surcharge pour la création d’un halo. Toutefois, à l’aide de cette technique, il peut être difficile de générer l’apparence d’un flash brillant à partir d’une source de lumière à point unique.

Les explosions peuvent être affichées dans une procédure de scène 3D similaire à celles utilisées pour le feu, les clignotements et les halos. Par exemple, votre application peut utiliser un panneau pour afficher une onde de choc et augmenter la prune de fumée lorsque l’explosion se produit. En même temps, votre application peut utiliser un ensemble de panneaux pour simuler les flammes. En outre, il peut positionner un seul panneau avant la scène pour ajouter un halo de lumière à la scène entière.

Les poutres d’énergie peuvent être simulées à l’aide de panneaux. Votre application peut également les afficher à l’aide de primitives définies comme listes de lignes ou bandes. Pour plus d’informations, consultez les [listes de lignes](line-lists.md) et les [bandes](line-strips.md).

Votre application peut créer des champs de force à l’aide de panneaux ou de primitives définis comme listes de triangles. Pour créer un champ force à partir de listes de triangles, définissez un ensemble de triangles disjoint dans une liste de triangles uniformément espacés sur la région couverte par le champ force. Les écarts entre les triangles permettent à l’utilisateur de voir la scène en arrière-plan, comme vous pouvez l’imaginer quand vous examinez un champ force. Appliquez une texture à la liste triangulaire qui donne aux triangles l’apparence de l’incandescence avec de l’énergie. Pour plus d’informations, consultez [listes de triangles](triangle-lists.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples alpha](alpha-examples.md)
</dt> </dl>

 

 



