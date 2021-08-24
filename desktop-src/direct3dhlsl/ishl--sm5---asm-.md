---
title: ishl (sm5 - asm)
description: Décalage vers la gauche. | ishl (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6908d12824c5aa84e04db38fb2462031bb2ae4a198700f98938456ecbd8619a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854209"
---
# <a name="ishl-sm5---asm"></a>ishl (sm5 - asm)

Décalage vers la gauche.



| ishl dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|--------------------------------------------------------|



 



| Élément                                                            | Description                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] contient les résultats de l’équipe de travail.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les valeurs 32 bits à décaler.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] le nombre de bits à décaler.<br/>        |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue un décalage au niveau du composant de chaque valeur 32 bits dans *src0* à gauche d’un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1*, en insérant 0. Les résultats de 32 bits par composant sont placés dans *dest*.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





