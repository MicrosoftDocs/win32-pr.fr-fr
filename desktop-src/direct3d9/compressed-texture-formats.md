---
description: Cette section contient des informations sur l’organisation interne des formats de texture compressés.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formats de texture compressés (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748797"
---
# <a name="compressed-texture-formats-direct3d-9"></a>Formats de texture compressés (Direct3D 9)

Cette section contient des informations sur l’organisation interne des formats de texture compressés. Vous n’avez pas besoin de ces détails pour utiliser des textures compressées, car vous pouvez utiliser des fonctions D3DX pour la conversion vers et depuis des formats compressés. Toutefois, ces informations sont utiles si vous souhaitez utiliser les données de surface compressées directement.

Direct3D utilise un format de compression qui divise les cartes de texture en blocs Texel 4x4. Si la texture ne contient pas de transparence-est opaque-ou si la transparence est spécifiée par une alpha de 1 bit, un bloc de 8 octets représente le bloc de la carte de texture. Si la carte de texture contient des texels transparents, à l’aide d’un canal alpha, un bloc de 16 octets le représente.

-   [Textures opaques et alpha 1 bits (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Textures avec canaux alpha (Direct3D 9)](textures-with-alpha-channels.md)

Toute texture unique doit spécifier que ses données sont stockées sous la forme de 64 ou 128 bits par groupe de 16 texels. Si les blocs 64 bits, c’est-à-dire le format DXT1, sont utilisés pour la texture, il est possible de mélanger les formats alpha opaque et 1 bits sur la base de chaque bloc au sein de la même texture. En d’autres termes, la comparaison de l’amplitude de l’entier non signé de la couleur \_ 0 et de la couleur \_ 1 est effectuée de manière unique pour chaque bloc de 16 texels.

Quand des blocs 128 bits sont utilisés, le canal alpha doit être spécifié dans explicite (format DXT2 ou DXT3) ou en mode interpolé (format DXT4 ou DXT5) pour la texture entière. Comme pour la couleur, lorsque le mode interpolé est sélectionné, huit alpha interpolés ou six modes alphabétiques interpolés peuvent être utilisés bloc par bloc. Là encore, la comparaison de magnitude des alpha \_ 0 et alpha \_ 1 est effectuée de manière unique sur une base bloc par bloc.

Le pas pour les formats DXTn est différent de ce qui a été retourné dans DirectX 7,0. Le tangage est maintenant mesuré en octets (et non pas en blocs). Par exemple, si vous avez une largeur de 16, vous obtiendrez un pas de quatre blocs (4 \* 8 pour DXT1, 4 \* pour DXT2-5).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources de texture compressées](compressed-texture-resources.md)
</dt> </dl>

 

 



