---
title: Break (SM4-ASM)
description: Déplace le point d’exécution vers l’instruction après le prochain ENDLOOP ou endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313663"
---
# <a name="break-sm4---asm"></a>Break (SM4-ASM)

Déplace le point d’exécution vers l’instruction après le prochain [ENDLOOP](endloop--sm4---asm-.md) ou [endswitch](endswitch--sm4---asm-.md).



| break |
|-------|



 

## <a name="remarks"></a>Notes

Le format de jeton contient le décalage de l’instruction **ENDLOOP** ou **endswitch** correspondante dans le nuanceur pour des raisons pratiques.

L’exemple suivant illustre l’instruction **break** .


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Cette instruction doit apparaître dans une **boucle** / **ENDLOOP** ou dans un **cas** d’un **commutateur** / **endswitch**.

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

 

 




