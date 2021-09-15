---
title: imad (SM4-ASM)
description: L’entier signé est multiplié et ajouté.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518625"
---
# <a name="imad-sm4---asm"></a>imad (SM4-ASM)

L’entier signé est multiplié et ajouté.



| imad dest \[ . Mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] , \[ - \] src2 \[ . Swizzle |
|---------------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] le résultat de l’opération.<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]valeur à multiplier avec *src1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[\]valeur à multiplier avec *src0*.<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[\]valeur à ajouter au produit de *src0* et *src1*.<br/> |



 

## <a name="remarks"></a>Notes

[Imul](imul--sm4---asm-.md) au niveau du composant des opérandes 32 bits *src0* et *src1* (signé), en conservant le résultat 32 bas (par composant) du résultat, suivi d’un [IAdd](iadd--sm4---asm-.md) de *src2*, ce qui produit le résultat de 32 bits (par composant) correct. Les résultats 32 bits sont placés dans *dest*.

Le modificateur de négation facultatif sur les opérandes source prend le complément à 2 avant d’effectuer une opération arithmétique.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





