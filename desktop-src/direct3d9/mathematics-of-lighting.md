---
description: Le modèle de lumière Direct3D couvre l’éclairage ambiant, diffus, spéculaire et émissif.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Mathématiques d’éclairage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683e320788d720883702ebfa56941b1a3a5cf090
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481096"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Mathématiques d’éclairage (Direct3D 9)

Le modèle de lumière Direct3D couvre l’éclairage ambiant, diffus, spéculaire et émissif. Il s’agit d’une flexibilité suffisante pour résoudre un large éventail de situations d’éclairage. Vous pouvez faire référence à la quantité totale de lumière dans une scène comme éclairage global et la calculer à l’aide de l’équation suivante.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



L' [éclairage ambiant (Direct3D 9)](ambient-lighting.md) est un éclairage constant. Elle est constante dans toutes les directions et elle colore tous les pixels d’un objet de la même façon. Il est rapide de calculer, mais laisse les objets à l’aspect plat et irréaliste. Pour voir comment l’éclairage ambiant est calculé par Direct3D, consultez éclairage ambiant (Direct3D 9).

L' [éclairage diffus (Direct3D 9)](diffuse-lighting.md) dépend à la fois de la direction de la lumière et de la surface de l’objet. Elle varie en fonction de la surface d’un objet en raison de la variation de la direction de la lumière et du vecteur de numération de surface variable. Il faut plus de temps pour calculer l’éclairage diffus, car il change pour chaque vertex d’objet, mais l’avantage de son utilisation est qu’il ombre les objets et leur donne une profondeur tridimensionnelle (3D). Pour voir comment l’éclairage diffus est calculé dans Direct3D, consultez lumière diffuse (Direct3D 9).

L' [éclairage spéculaire (Direct3D 9)](specular-lighting.md) identifie les surbrillances spéculaires brillantes qui se produisent lorsque la lumière atteint une surface d’objet et renvoie vers l’appareil photo. Elle est plus intense que la lumière diffuse et s’arrête plus rapidement sur l’aire de l’objet. Le calcul de l’éclairage spéculaire prend plus de temps que l’éclairage diffus, mais l’avantage de son utilisation est qu’il ajoute des détails significatifs à une surface. Pour voir comment l’éclairage spéculaire est calculé dans Direct3D, consultez éclairage spéculaire (Direct3D 9).

L' [éclairage émissif (Direct3D 9)](emissive-lighting.md) est une lumière émise par un objet. par exemple, une lueur. Pour voir comment l’éclairage émissif est calculé dans Direct3D, consultez éclairage émissif (Direct3D 9).

L’éclairage réaliste peut être obtenu en appliquant chacun de ces types d’éclairage à une scène 3D. Les valeurs calculées pour les composants ambiant, émissif et diffuse sont générées comme couleur de vertex diffuse ; la valeur du composant d’éclairage spéculaire est sortie comme couleur de vertex spéculaire. Les valeurs de lumière ambiante, diffuse et spéculaire peuvent être affectées par un facteur d’atténuation et de focalisation d’un éclairage donné. Pour plus d’informations sur le fonctionnement de l’atténuation, consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).

Pour obtenir un effet d’éclairage plus réaliste, vous ajoutez des lumières supplémentaires. Toutefois, le rendu de la scène est plus long. Pour obtenir tous les effets souhaités d’un concepteur, certains jeux utilisent plus de puissance de processeur que ce qui est généralement disponible. Dans ce cas, il est courant de réduire au minimum le nombre de calculs d’éclairage en utilisant des cartes d’éclairage et des cartes d’environnement pour ajouter de l’éclairage à une scène tout en utilisant des cartes de texture.

L’éclairage est calculé dans l’espace de l’appareil photo. Pour voir comment les transformations d’éclairage sont calculées, consultez [transformations d’espace de caméra (Direct3D 9)](camera-space-transformations.md). L’éclairage optimisé peut être calculé dans l’espace du modèle, lorsque des conditions spéciales existent : les vecteurs normaux sont déjà normalisés (D3DRS \_ NORMALIZENORMALS a la valeur true), la fusion des vertex n’est pas nécessaire, les matrices de transformation sont orthogonales, et ainsi de suite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lumières et matériaux](lights-and-materials.md)
</dt> </dl>

 

 



