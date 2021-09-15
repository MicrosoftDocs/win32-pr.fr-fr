---
title: dcl_stream (SM5-ASM)
description: Déclare un flux de sortie de nuanceur Geometry.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524745"
---
# <a name="dcl_stream-sm5---asm"></a>\_flux DCL (SM5-ASM)

Déclare un flux de sortie de nuanceur Geometry.



| \_flux DCL m\# |
|-----------------|



 



| Élément                                                       | Description                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*lecteur\#*<br/> | \[dans le \] flux 0.. 3 (M0.. m3).<br/> |



 

## <a name="remarks"></a>Notes

Un flux donné ne peut être déclaré qu’une seule fois.

Si aucun flux n’est déclaré, les déclarations de topologie de sortie et de sortie sont supposées être pour le flux 0.

Le premier **\_ flux DCL** ne peut pas apparaître après des instructions de **\_ sortie DCL** ou **DCL \_ outputTopology** .

Les instructions de **\_ sortie DCL** ou **DCL \_ outputToplogy** après toute instruction du **\_ flux DCL** m \# définissent les sorties du flux m \# .

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





