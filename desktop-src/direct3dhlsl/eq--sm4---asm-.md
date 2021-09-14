---
title: EQ (SM4-ASM)
description: Comparaison d’égalité des points à virgule flottante vectorielle.
ms.assetid: 925578E4-0161-45A9-840F-14AA65FF4F33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f47dc7bda7b1c61c251ace061fc75897788b968
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414458"
---
# <a name="eq-sm4---asm"></a>EQ (SM4-ASM)

Comparaison d’égalité des points à virgule flottante vectorielle.



| EQ dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------------------------------------|



 



| Élément                                                            | Description                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le composant à comapre à *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[dans \] le composant à comapre à *src0*.<br/>         |



 

## <a name="remarks"></a>Notes

Effectue la comparaison float (*src0*  ==  *src1*) pour chaque composant et écrit le résultat dans *dest*.

Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant. Sinon, 0x0000000 est retourné.

Les dénormes sont vidées avant la comparaison (les registres source d’origine ne sont pas touchés). + 0 est égal à-0. La comparaison avec NaN retourne false.

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

 

 





