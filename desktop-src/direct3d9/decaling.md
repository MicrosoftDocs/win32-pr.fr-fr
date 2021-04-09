---
description: Les applications Direct3D utilisent le décalqueing pour contrôler les pixels d’une image primitive particulière qui sont dessinés sur la surface cible de rendu. Les applications appliquent des dépassements aux images de primitives pour permettre l’affichage correct de polygones polygones.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Décalqueing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108751"
---
# <a name="decaling-direct3d-9"></a>Décalqueing (Direct3D 9)

Les applications Direct3D utilisent le décalqueing pour contrôler les pixels d’une image primitive particulière qui sont dessinés sur la surface cible de rendu. Les applications appliquent des dépassements aux images de primitives pour permettre l’affichage correct de polygones polygones.

Par exemple, lorsque vous appliquez des marques de pneu et des lignes jaunes à une chaussée, les marquages doivent apparaître directement en haut de la route. Toutefois, les valeurs z des marquages et de la route sont les mêmes. Par conséquent, il se peut que la mémoire tampon de profondeur ne produise pas une séparation nette entre les deux. Certains pixels de la primitive arrière peuvent être rendus au-dessus de la primitive avant et vice versa. L’image résultante semble en scintillement du cadre au frame. Cet effet est appelé *z-combat* ou *flimmering*.

Pour résoudre ce problème, utilisez un gabarit pour masquer la section de la primitive de retour où le décalcomanie s’affichera. Désactivez la mise en mémoire tampon z et affichez l’image de la primitive avant dans la zone masquée de la surface de rendu-cible.

Bien que la combinaison de plusieurs textures puisse être utilisée pour résoudre ce problème, cela limite le nombre d’autres effets spéciaux que votre application peut produire. L’utilisation de la mémoire tampon de stencil pour appliquer des dépassements libère des étapes de fusion de texture pour d’autres effets.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques de tampon de stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



