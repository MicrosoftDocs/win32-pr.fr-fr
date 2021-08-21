---
title: deriv_rtx_fine (SM5-ASM)
description: Calcule le taux de modification des composants. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6666750be76d673ddc6c5f0d66d23131096812c93b71be52eb7e0f6ebb403ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792652"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>Deriv \_ RTX \_ fine (SM5-ASM)

Calcule le taux de modification des composants.



| Deriv \_ RTX \_ fine \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|--------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants de l’opération.<br/>             |



 

## <a name="remarks"></a>Remarques

Cette instruction calcule le taux de modification du contenu de chaque composant float32 de *src0* (Swizzle), en ce qui concerne la direction renderTarget x (RTX) ou l’axe des renderTarget y (consultez [Deriv \_ propriété \_ fine](deriv-rty-fine--sm5---asm-.md)). Chaque pixel dans le tampon 2x2 obtient une paire unique de calculs de dérivés x/y

Les données de l’appel de nuanceur de pixels actuel participent toujours au calcul de la dérivée demandée. Dans le quadruple pixel Quad, le pixel actuel se trouve dans, la dérivée x est le delta de la ligne de 2 pixels, y compris le pixel actuel. Le dérivé de y est le delta de la colonne de 2 pixels, y compris le pixel actuel. Il n’existe aucune spécification qui dicte la manière dont les quadruples 2x2 sont alignés ou en mosaïque sur une primitive.

Les dérivés sont calculés à un niveau précis (calcul unique de la paire de dérivés x/y pour chaque pixel dans un quadruple quad). Cette instruction et [Deriv \_ propriété \_ fine](deriv-rty-fine--sm5---asm-.md) sont des alternatives à [Deriv \_ RTX \_ grossiste](deriv-rtx-coarse--sm5---asm-.md) et [Deriv \_ propriété \_ grossiste](deriv-rty-coarse--sm5---asm-.md). Ces \_ \_ instructions dérivées grossières et fine remplacent **Deriv \_ RTX** ces \_ instructions de gros grain et de \_ dérivées fine remplacent les **Deriv \_ RTX** et **Deriv \_ propriété** des modèles de nuanceur précédents.

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

 

 





