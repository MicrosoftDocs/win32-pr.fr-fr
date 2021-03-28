---
title: cut_stream (SM5-ASM)
description: Instruction de nuanceur Geometry qui termine la topologie primitive actuelle au niveau du flux spécifié, si des vertex y ont été émis, et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry au niveau de ce flux.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381143"
---
# <a name="cut_stream-sm5---asm"></a>couper \_ le flux (SM5-ASM)

Instruction de nuanceur Geometry qui termine la topologie primitive actuelle au niveau du flux spécifié, si des vertex y ont été émis, et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry au niveau de ce flux.



| couper le \_ streamIndex de flux |
|-------------------------|



 



| Élément                                                                                                               | Description                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[dans \] l’index de flux.<br/> |



 

## <a name="remarks"></a>Notes

Lorsque cette instruction est exécutée, toute topologie précédemment émise par l’appel de nuanceur Geometry est terminée. Si le nombre de vertex émis pour la topologie primitive précédente est insuffisant, ils sont ignorés. Étant donné que les seules topologies de sortie disponibles pour le nuanceur Geometry sont PointList, linestrip et TriangleStrip, il n’y a jamais de vertex restants.

*streamIndex* doit être une valeur immédiate \[ comprise entre 0 et 3 \] pour un flux déclaré.

Après la topologie précédente, le cas échéant, cette instruction provoque le début d’une nouvelle topologie, à l’aide de la topologie déclarée comme sortie du nuanceur Geometry.

### <a name="restrictions"></a>Restrictions

-   Cette instruction s’applique uniquement au nuanceur Geometry.
-   **le \_ flux réduit** peut apparaître un nombre quelconque de fois dans le nuanceur Geometry, y compris dans le contrôle de flux.
-   Si le nuanceur Geometry se termine et que les vertex ont été émis, la topologie qu’ils génèrent est terminée, comme si une instruction de **\_ flux réduit** avait été exécutée en tant que dernière instruction.
-   Si les flux n’ont pas été déclarés, vous devez utiliser **le \_ flux** [Cut](cut--sm4---asm-.md) au lieu de Cut.

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

 

 





