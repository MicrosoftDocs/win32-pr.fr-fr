---
description: Pour qu’une application affiche de manière réaliste une scène 3D, elle doit prendre en compte l’effet que les sources de lumière ont sur l’apparence de la scène.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Mise en correspondance de la lumière avec les textures (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513102"
---
# <a name="light-mapping-with-textures-direct3d-9"></a>Mise en correspondance de la lumière avec les textures (Direct3D 9)

Pour qu’une application affiche de manière réaliste une scène 3D, elle doit prendre en compte l’effet que les sources de lumière ont sur l’apparence de la scène. Bien que les techniques telles que l’ombrage plat et l’ombrage Gouraud soient des outils précieux à cet égard, elles peuvent être insuffisantes pour répondre à vos besoins. Direct3D prend en charge la fusion multipasse et plusieurs textures. Ces fonctionnalités permettent à votre application de restituer des scènes avec une apparence plus réaliste que les scènes rendues uniquement avec des techniques d’ombrage. En appliquant une ou plusieurs cartes de lumière, votre application peut mapper les zones de lumière et d’ombre sur ses Primitives.

Une carte de lumière est une texture ou un groupe de textures qui contient des informations sur l’éclairage dans une scène 3D. Vous pouvez stocker les informations d’éclairage dans les valeurs alpha de la carte de lumière, dans les valeurs de couleur, ou dans les deux.

Si vous implémentez le mappage de lumière à l’aide de la fusion de texture multipasse, votre application doit restituer la carte de lumière sur ses primitives au premier passage. Il doit utiliser une deuxième passe pour restituer la texture de base. La seule exception est le mappage de lumière spéculaire. Dans ce cas, restituez d’abord la texture de base. Ajoutez ensuite la carte de lumière.

La fusion de plusieurs textures permet à votre application de restituer la carte de lumière et la texture de base en une seule passe. Si le matériel de l’utilisateur fournit une fusion multiple de texture, votre application doit en tirer parti lors de l’exécution du mappage de la lumière. Cela améliore considérablement les performances de votre application.

Grâce aux cartes de lumière, une application Direct3D peut obtenir un large éventail d’effets d’éclairage lors du rendu de Primitives. Il peut également mapper des lumières monochromes et colorées dans une scène, mais il peut également ajouter des détails tels que des surbrillances spéculaires et un éclairage diffus.

Des informations sur l’utilisation de la fusion de texture Direct3D pour effectuer un mappage de lumière sont présentées dans les rubriques suivantes.

-   [Cartes de lumière monochromes (Direct3D 9)](monochrome-light-maps.md)
-   [Cartes de lumière de couleur (Direct3D 9)](color-light-maps.md)
-   [Cartes de lumière spéculaire (Direct3D 9)](specular-light-maps.md)
-   [Cartes de lumière diffuse (Direct3D 9)](diffuse-light-maps.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion de texture](texture-blending.md)
</dt> </dl>

 

 



