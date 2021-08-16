---
title: Mosaïque de mémoires tampons
description: Une ressource de mémoire tampon est divisée en mosaïques de 64 Ko, avec un espace vide dans la dernière vignette si la taille n’est pas un multiple de 64 Ko.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36352f492efb88bf220035d737b5767ef086e74ab91ffb4228d7734f838425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734241"
---
# <a name="buffer-tiling"></a>Mosaïque de mémoires tampons

Une ressource de [mémoire tampon](overviews-direct3d-11-resources-buffers.md) est divisée en mosaïques de 64 Ko, avec un espace vide dans la dernière vignette si la taille n’est pas un multiple de 64 Ko.

Les mémoires tampons structurées ne doivent pas avoir de contrainte sur le STRIDE à présenter en mosaïque. Toutefois, les optimisations de performances possibles dans le matériel pour l’utilisation de [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) peuvent être sacrifiées en les mettant en mosaïque en premier lieu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mode de mosaïque de la zone d’une ressource en mosaïque](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 