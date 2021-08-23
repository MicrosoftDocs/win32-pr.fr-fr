---
title: deriv_rtx_coarse (SM5-ASM)
description: Calcule le taux de modification des composants. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50066fe58c3d0a0cdd903de9fbb479a8fbab2c3a20c622ebca138c0937aaf0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986639"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>Deriv \_ RTX \_ grossiste (SM5-ASM)

Calcule le taux de modification des composants.



| Deriv \_ RTX \_ grossiste \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|----------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants de l’opération.<br/>             |



 

## <a name="remarks"></a>Remarques

Cette instruction calcule le taux de modification du contenu de chaque composant float32 de *src0* (Swizzle), en ce qui concerne la direction renderTarget x (RTX) ou renderTarget y (voir [Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md)). Une seule paire dérivée x, y est calculée pour chaque tampon 2x2 de pixels.

Les données de l’appel de nuanceur de pixels actuel peuvent ou non participer au calcul de la dérivée demandée, car le dérivé est calculé une seule fois par 2x2 Quad. Par exemple, la dérivée x peut être un Delta à partir de la ligne supérieure de pixels, tandis que la direction y ([Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md)) peut être un delta de la colonne de gauche de pixels. Le calcul exact est effectué par le fournisseur de matériel. Il n’y a pas non plus de spécification indiquant comment les quadruples 2x2 sont alignés ou en mosaïque sur une primitive.

Les dérivés sont calculés à un niveau grossier, une fois par Quad pixel Quad. Cette instruction et [Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md) sont des alternatives à [Deriv \_ RTX \_ fine](deriv-rtx-fine--sm5---asm-.md) et [Deriv \_ propriété \_ ](deriv-rty-fine--sm5---asm-.md). Ces \_ \_ instructions dérivées grossières et fine remplacent **Deriv \_ rtxderiv \_ propriété** des modèles de nuanceur précédents.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





