---
title: utof (SM4-ASM)
description: Entier non signé pour la conversion à virgule flottante.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd5e69476c77ee71e25c3e2286ddd53cc01027197b7ad9d83ed723438a93882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283007"
---
# <a name="utof-sm4---asm"></a>utof (SM4-ASM)

Entier non signé pour la conversion à virgule flottante.



| utof dest \[ . Mask \] , src0 \[ . Swizzle\] |
|--------------------------------------|



 



| Élément                                                            | Description                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] les composants à convertir.<br/>                  |



 

## <a name="remarks"></a>Notes

*src0* doit contenir un entier 4 tuples non signé 32 bits. Après l’exécution de l’instruction, *dest* contient un tuple à virgule flottante. La conversion est effectuée par composant.

Lorsqu’une valeur d’entrée d’entier est trop grande pour être représentée exactement au format à virgule flottante, arrondir au mode pair le plus proche.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





