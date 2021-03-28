---
title: ftou (SM4-ASM)
description: Conversion d’un entier non signé en virgule flottante.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313645"
---
# <a name="ftou-sm4---asm"></a>ftou (SM4-ASM)

Conversion d’un entier non signé en virgule flottante.



| ftou dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------|



 



| ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------|



 



| Élément                                                            | Description                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de l’opération. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] la valeur à convertir.<br/>                        |



 

## <a name="remarks"></a>Notes

La conversion est effectuée par composant. L’arrondi est toujours effectué vers zéro, suivant la Convention C pour les conversions de float en int.

Les applications qui requièrent une sémantique d’arrondi différente peuvent appeler les instructions **Round** avant d’effectuer un cast en Integer.

Les entrées sont ancrées à la plage \[ 0.0 f... 4294967295.999 f \] avant la conversion, et les valeurs NaN d’entrée produisent un résultat zéro.

Les modificateurs de valeur absolue et de négation facultatifs sont appliqués aux valeurs sources avant la conversion.

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

 

 





