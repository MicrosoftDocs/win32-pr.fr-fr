---
title: RETC (SM4-ASM)
description: Retour conditionnel.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d65cf64c3c1fb7945f93053f280be3eb3bd9d5fe76e34f30102316b1f1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853739"
---
# <a name="retc-sm4---asm"></a>RETC (SM4-ASM)

Retour conditionnel.



| RETC { \_ z \|\_NZ} src0. sélectionner le \_ composant |
|----------------------------------------|



 



| Élément                                                            | Description                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le registre pour tester la condition.<br/> |



 

## <a name="remarks"></a>Remarques

Si, dans une sous-routine, cette instruction retourne de manière conditionnelle à l’instruction après l’appel. Si elle ne se trouve pas à l’intérieur d’une sous-routine, cette instruction termine l’exécution du programme.

L’exemple suivant montre comment utiliser cette instruction.

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a>Restrictions

-   **RETC** peut apparaître n’importe où dans un programme, un nombre quelconque de fois.
-   La dernière instruction d’un programme ou d’une sous-routine principale ne peut pas être un **RETC \_ z** ou **RETC \_ NZ**. Au lieu de cela, la [RET](ret--sm4---asm-.md) inconditionnelle peut être utilisée.
-   Le registre 32 bits fourni par *src0* est testé à un niveau binaire. Si un bit est différent de zéro, la valeur **RET \_ NZ** retourne. Si tous les bits sont nuls, **RETC \_ z** retourne.

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

 

 





