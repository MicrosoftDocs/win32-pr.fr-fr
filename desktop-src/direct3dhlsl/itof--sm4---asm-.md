---
title: itof (SM4-ASM)
description: Entier signé dans la conversion à virgule flottante.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841669"
---
# <a name="itof-sm4---asm"></a>itof (SM4-ASM)

Entier signé dans la conversion à virgule flottante.



| itof dest \[ . Mask \] , \[ - \] src0 \[ . Swizzle\] |
|-------------------------------------------|



 



| Élément                                                            | Description                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] contient le résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] contient la valeur à convertir.<br/>        |



 

## <a name="remarks"></a>Notes

Cette instruction de conversion de type entier à virgule flottante suppose que *src0* contient un entier 32 bits signé de 4 tuples. Après l’exécution de l’instruction, *dest* contient un tuple à virgule flottante.

La conversion est effectuée par composant.

Lorsqu’une valeur d’entrée d’entier est trop grande pour être représentée exactement au format à virgule flottante, l’arrondi au mode pair le plus proche est fortement recommandé, mais pas obligatoire.

Le modificateur de négation facultatif sur l’opérande source prend le complément à 2 avant d’effectuer une opération arithmétique.

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

 

 





