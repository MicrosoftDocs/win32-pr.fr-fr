---
title: if (SM4-ASM)
description: Branche basée sur le ou le résultat logique.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990705"
---
# <a name="if-sm4---asm"></a>if (SM4-ASM)

Branche basée sur le ou le résultat logique.



| Si { \_ z \|\_NZ} src0. sélectionner le \_ composant |
|--------------------------------------|



 



| Élément                                                            | Description                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] contient le composant sur lequel tester la condition.<br/> |



 

## <a name="remarks"></a>Notes

Le format de jeton contient le décalage de l’instruction ENDIF correspondante dans le nuanceur pour des raisons pratiques.

L’exemple suivant montre comment utiliser cette instruction.

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a>Restrictions

-   Les opérandes sources (si 4 vecteurs de composant) doivent utiliser un sélecteur de composant unique.
-   Le registre 32 bits fourni par *src0* est testé à un niveau binaire. Si un bit est différent de zéro, **si \_ z** est true. Si tous les bits sont nuls, si la valeur **\_ NZ** est true.
-   Les blocs de contrôle de Flow peuvent imbriquer jusqu’à 64 de profondeur par sous-routine (et main). Le compilateur HLSL ne génère pas de sous-routines qui dépassent cette limite. Le comportement des instructions de workflow de contrôle au-delà de 64 niveaux de profondeur (par sous-routine) n’est pas défini.

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

 

 





