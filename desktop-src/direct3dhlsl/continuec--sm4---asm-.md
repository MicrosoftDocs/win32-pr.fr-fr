---
title: continuec (SM4-ASM)
description: Continue l’exécution de manière conditionnelle au début de la boucle en cours.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d909c199dc0ceaa4e5498429f1ac3a136d3fb75d930e392d7f6fd8230e5b49b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909056"
---
# <a name="continuec-sm4---asm"></a>continuec (SM4-ASM)

Continue l’exécution de manière conditionnelle au début de la boucle en cours.



| continuec { \_ z \|\_NZ} src0. sélectionner le \_ composant |
|---------------------------------------------|



 



| Terme                                                            | Description                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le composant sur lequel tester la condition.<br/> |



 

## <a name="remarks"></a>Remarques

**continuec** peut être utilisé uniquement à l’intérieur d’une [boucle](loop--sm4---asm-.md) ou d’un [ENDLOOP](endloop--sm4---asm-.md).

L’exemple suivant montre comment utiliser l’instruction **continuec** .


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



Le format de jeton contient le décalage de l’instruction de boucle correspondante dans le nuanceur pour des raisons pratiques.

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
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





