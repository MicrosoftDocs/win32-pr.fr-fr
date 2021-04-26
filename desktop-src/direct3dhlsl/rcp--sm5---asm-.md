---
title: RCP (SM5-ASM)
description: Réciproque au niveau du composant.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998246"
---
# <a name="rcp-sm5---asm"></a>RCP (SM5-ASM)

Réciproque au niveau du composant.



| RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------|



 



| Élément                                                            | Description                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats<br/> *dest*  =  . **1.0 f**  /  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le nombre à prendre la réciproque de.<br/>                             |



 

## <a name="remarks"></a>Remarques

Utilisez cette instruction pour réduire la précision réciproque, indépendamment des exigences strictes pour la Division.

L’erreur relative maximale est 2-21. (La tolérance d’erreur correspond simplement à rsq)

Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres.



| *src*  | **-INF** | **-F** | **-dénorme** | **-0** | **+0** | **+ dénorme** | **+ F** | **+ INF** | **NaN** |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| *dest* | -0       | -F     | -inf        | -inf   | +inf   | +inf        | + F     | +0       | NaN     |



 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
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

 

 





