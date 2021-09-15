---
title: Objets modèle de nuanceur 5,1
description: Les objets suivants ont été ajoutés au nuanceur modèle 5,1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ce272e789501e21f5866be37f56daf31bc829
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524512"
---
# <a name="shader-model-51-objects"></a>Objets modèle de nuanceur 5,1

Les objets suivants ont été ajoutés au nuanceur modèle 5,1.

Pour les [vues](/windows/desktop/direct3d11/rasterizer-order-views) de l’ordre du rastériseur (disponible dans D3D 11.3 et D3D12), les objets suivants sont nouveaux et sont uniquement autorisés dans le nuanceur de pixels. Notez que les méthodes qu’ils prennent en charge sont identiques aux objets UAV correspondants.



| Objet rastériseur                                   | Objet UAV                                                              |
|------------------------------------|---------------------------------------------------------------|
| RasterizerOrderedBuffer            | [**RWBuffer**](sm5-object-rwbuffer.md)                       |
| RasterizerOrderedByteAddressBuffer | [**RWByteAddressBuffer**](sm5-object-rwbyteaddressbuffer.md) |
| RasterizerOrderedStructuredBuffer  | [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md)   |
| RasterizerOrderedTexture1D         | [**RWTexture1D**](sm5-object-rwtexture1d.md)                 |
| RasterizerOrderedTexture1DArray    | [**RWTexture1DArray**](sm5-object-rwtexture1darray.md)       |
| RasterizerOrderedTexture2D         | [**RWTexture2D**](sm5-object-rwtexture2d.md)                 |
| RasterizerOrderedTexture2DArray    | [**RWTexture2DArray**](sm5-object-rwtexture2darray.md)       |
| RasterizerOrderedTexture3D         | [**RWTexture3D**](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle de nuanceur 5,1](shader-model-5-1.md)
</dt> <dt>

[Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
