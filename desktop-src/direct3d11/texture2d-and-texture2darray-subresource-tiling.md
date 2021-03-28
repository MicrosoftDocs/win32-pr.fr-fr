---
title: Restitution des sous-ressources Texture2D et Texture2DArray sous forme de mosaïque
description: Ces tableaux montrent comment les sous-ressources Texture2D et Texture2DArray sont présentées en mosaïque.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382283"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Restitution des sous-ressources Texture2D et Texture2DArray sous forme de mosaïque

Ces tableaux montrent comment les sous-ressources [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) sont présentées en mosaïque. Les valeurs de ces tables ne comptent pas la fin de la compression MIP.

Ce tableau montre comment les sous-ressources [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) avec un nombre d’échantillons de 1 sont en mosaïque.



| Bits/pixel (1 échantillon/pixel) | Dimensions de la mosaïque (pixels, WxH) |
|-----------------------------|-------------------------------|
| 8                           | 256 x 256                       |
| 16                          | 256 x 128                       |
| 32                          | 128 x 128                       |
| 64                          | 128x64                        |
| 128                         | 64 x 64                         |
| BC1, 4                       | 512x256                       |
| BC2, 3, 5, 6, 7                 | 256 x 256                       |



 

Les nombres de bits de format non pris en charge avec les ressources en mosaïque sont les formats 96 BPP, les formats vidéo, le \_ format dxgi \_ R1 \_ UNORM, le \_ format dxgi \_ R8G8 B8G8 UNORM et le \_ \_ format dxgi \_ \_ \_ \_ R8R8 G8B8 UNORM.

Ce tableau montre comment les sous-ressources [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) avec différents nombres d’échantillons sont en mosaïque.



| Nombre d’échantillons           | Diviser les dimensions de mosaïque ci-dessus par (WxH) |
|-----------------------------|-------------------------------|
| 1                           | individuelles                           |
| 2                           | 2 x 1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Seuls les nombres d’échantillons 1 et 4 sont requis (et autorisés) pour être pris en charge avec les ressources en mosaïque. Les ressources en mosaïque ne prennent pas en charge 2, 8 et 16, même si elles sont affichées.

Les implémentations peuvent choisir de prendre en charge les modes d’échantillonnage 2, 8 et/ou 16 pour les ressources non en mosaïque, même si la ressource en mosaïque ne les prend pas en charge.

Les ressources en mosaïque avec des nombres d’échantillons supérieurs à 1 ne peuvent pas utiliser les formats 128 BPP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mode de mosaïque de la zone d’une ressource en mosaïque](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 