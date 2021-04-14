---
title: Restitution de la sous-ressource Texture3D sous forme de mosaïque
description: Ce tableau montre comment les sous-ressources Texture3D sont présentées en mosaïque.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991025"
---
# <a name="texture3d-subresource-tiling"></a>Restitution de la sous-ressource Texture3D sous forme de mosaïque

Ce tableau montre comment les sous-ressources [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) sont présentées en mosaïque. Les valeurs de cette table ne comptent pas la fin de la compression MIP.

Cette table prend la mosaïque [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et divise les dimensions x/y par 4 et ajoute 16 couches de profondeur. Toutes les vignettes du premier plan (plan 2D des vignettes définissant les 16 premières couches de profondeur) apparaissent avant les plans suivants.

> [!Note]  
> La prise en charge de [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) dans les ressources en mosaïque n’est pas exposée dans l’implémentation initiale des ressources en mosaïque, mais les formes de mosaïque souhaitées sont répertoriées ici, car le support peut être pris en compte dans une version ultérieure.

 



| Bits/pixel (1 échantillon/pixel) | Dimensions de la mosaïque (pixels, WxHxD) |
|-----------------------------|---------------------------------|
| 8                           | 64x32x32                        |
| 16                          | 32x32x32                        |
| 32                          | 32x32x16                        |
| 64                          | 32x16x16                        |
| 128                         | 16x16x16                        |
| BC1, 4                       | 128x64x16                       |
| BC2, 3, 5, 6, 7                 | 64x64x16                        |



 

Les nombres de bits de format non pris en charge avec les ressources en mosaïque sont les formats 96 BPP, les formats vidéo, le \_ format dxgi \_ R1 \_ UNORM, le \_ format dxgi \_ R8G8 B8G8 UNORM et le \_ \_ format dxgi \_ \_ \_ \_ R8R8 G8B8 UNORM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mode de mosaïque de la zone d’une ressource en mosaïque](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 