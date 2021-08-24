---
title: RET (SM4-ASM)
description: Instruction return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7482c2c7351944824e2590f5c87dac63bde8f639a5ad42dffdfc71e4134603b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853749"
---
# <a name="ret-sm4---asm"></a>RET (SM4-ASM)

Instruction return.



| Av |
|-----|



 

## <a name="remarks"></a>Remarques

Si, dans une sous-routine, retourne à l’instruction après l’appel. Dans le cas contraire à l’intérieur d’une sous-routine, terminez l’exécution du programme.

L’exemple suivant montre comment utiliser cette instruction.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a>Restrictions

-   **RET** peut apparaître n’importe où dans un programme, un nombre quelconque de fois.
-   Si une instruction d' [étiquette](label--sm4---asm-.md) apparaît dans un nuanceur, elle doit être précédée d’une commande **RET** qui n’est imbriquée dans aucune instruction de contrôle de Flow.
-   S’il existe des sous-routines dans un nuanceur, la dernière instruction du nuanceur doit être un **RET**.

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

 

 




