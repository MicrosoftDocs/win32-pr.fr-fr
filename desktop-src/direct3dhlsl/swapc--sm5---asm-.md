---
title: swapc (SM5-ASM)
description: Effectue un échange conditionnel au niveau du composant des valeurs entre deux registres d’entrée.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d09d52bd497c7819500c11c4464907e4a7854bb305ed0e31d53b897ba4cf7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486259"
---
# <a name="swapc-sm5---asm"></a>swapc (SM5-ASM)

Effectue un échange conditionnel au niveau du composant des valeurs entre deux registres d’entrée.



| swapc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Élément                                                               | Description                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[dans \] Register avec des masques d’écriture non vides arbitraires. Doit être différent de *dest1*.<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[dans \] Register avec des masques d’écriture non vides arbitraires. Doit être différent de *dest0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[dans \] fournit 4 conditions. Une valeur entière différente de zéro signifie **true**. <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[dans l' \] une des valeurs à permuter.<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/>    | \[dans l' \] une des valeurs à permuter.<br/>                                              |



 

## <a name="remarks"></a>Remarques

L’encodage de cette instruction tente d’exprimer compactement plusieurs swaps conditionnels parallèles de scalaires dans des registres de composants de 2 4, avec une flexibilité mineure dans la disposition des paires de nombres impliquées dans l’échange.

Le choix du Registre et de la valeur pour *src0*, *src1* et *src2* sont sans contrainte, comme [MOVC](movc--sm4---asm-.md).

La sémantique de cette instruction peut être décrite par les opérations équivalentes à l’aide de l’instruction **MOVC** . Le pire cas est illustré dans l’exemple suivant, en s’assurant que les registres de destination ne sont pas mis à jour jusqu’à la fin.

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

Vous pouvez choisir le mode de traitement de la tâche, si ce n’est pas direct. Par exemple, le même effet peut être obtenu à l’aide d’une séquence allant jusqu’à 4 swaps conditionnels scalaires simples ou, comme ci-dessus, deux instructions **MOVC** de vecteurs, plus toute surcharge pour s’assurer que les valeurs sources ne sont pas écrasées par des opérations antérieures au milieu de l’expansion.

Utilisez cette instruction pour le tri.

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

 

 





