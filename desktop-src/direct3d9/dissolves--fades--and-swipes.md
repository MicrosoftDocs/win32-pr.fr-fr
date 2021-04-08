---
description: De plus en plus, les applications utilisent des effets spéciaux qui sont couramment utilisés dans les films et les vidéos, tels que les dissolutions, les balayages et les fondus.
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: Dissoudre, fondu et balayage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ad837ea846ca43d61102ce426d415270d2f27f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746860"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a>Dissoudre, fondu et balayage (Direct3D 9)

De plus en plus, les applications utilisent des effets spéciaux qui sont couramment utilisés dans les films et les vidéos, tels que les dissolutions, les balayages et les fondus.

Dans une solution, une image est progressivement remplacée par une autre dans une séquence lisse de frames. Bien que Direct3D fournisse des méthodes d’utilisation de plusieurs textures de fusion pour obtenir le même effet, les applications qui utilisent la mémoire tampon de stencil pour les conversions peuvent utiliser des fonctionnalités de fusion de texture pour d’autres effets pendant qu’ils effectuent une dissolution.

Lorsque votre application effectue une dissolution, elle doit restituer deux images différentes. Elle utilise la mémoire tampon de stencil pour contrôler les pixels de chaque image qui sont dessinés sur la surface cible de rendu. Vous pouvez définir une série de masques de stencil et les copier dans la mémoire tampon de stencil sur des frames successifs. Vous pouvez également définir un masque de gabarit de base pour le premier frame et le modifier de façon incrémentielle.

Au début de la dissolution, votre application définit la fonction de stencil et le masque de stencil afin que la plupart des pixels de l’image de départ passent le test de stencil. La plupart des pixels de l’image finale doivent faire échouer le test du stencil. Sur des frames successifs, le masque du gabarit est mis à jour afin que le nombre de pixels de l’image de départ soit inférieur ou inférieur au test. Au fur et à mesure que les images progressent, le test n’est pas limité à moins de pixels dans l’image finale. De cette manière, votre application peut effectuer une dissolution à l’aide d’un modèle de dissolution arbitraire.

Le fondu ou la dégradation est un cas particulier de résolution. En cas de fondu, la mémoire tampon du stencil est utilisée pour la résolution d’une image noire ou blanche en rendu d’une scène 3D. Le fondu est l’inverse, votre application commence par un rendu d’une scène 3D et est convertie en noir ou blanc. Le fondu peut être effectué à l’aide de n’importe quel modèle arbitraire que vous souhaitez utiliser.

Les applications Direct3D utilisent une technique similaire pour les balayages. Par exemple, lorsqu’une application effectue un balayage de gauche à droite, l’image de fin apparaît progressivement sur l’image de départ, de gauche à droite. Comme dans une solution, vous devez définir une série de masques de stencil chargés dans la mémoire tampon de stencil sur des frames successifs, ou modifier successivement le masque de début du stencil. Les masques de stencil sont utilisés pour désactiver l’écriture des pixels à partir de l’image de départ et pour activer l’écriture des pixels à partir de l’image finale.

Un balayage est un peu plus complexe qu’un fondu dans le sens où votre application doit lire les pixels de l’image finale dans l’ordre inverse du balayage. Autrement dit, si le balayage se déplace de gauche à droite, votre application doit lire les pixels de l’image finale de droite à gauche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques de tampon de stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



