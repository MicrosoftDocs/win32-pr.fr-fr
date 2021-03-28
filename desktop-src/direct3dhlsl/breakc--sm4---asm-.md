---
title: breakc (SM4-ASM)
description: Déplace de manière conditionnelle le point d’exécution vers l’instruction après le prochain ENDLOOP ou endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381185"
---
# <a name="breakc-sm4---asm"></a>breakc (SM4-ASM)

Déplace de manière conditionnelle le point d’exécution vers l’instruction après le prochain [ENDLOOP](endloop--sm4---asm-.md) ou [endswitch](endswitch--sm4---asm-.md).



| breakc { \_ z \|\_NZ} src0. sélectionner le \_ composant |
|------------------------------------------|



 



| Élément                                                            | Description                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le composant sur lequel tester la condition.<br/> |



 

## <a name="remarks"></a>Notes

Le format de jeton contient le décalage de l’instruction **ENDLOOP** correspondante dans le nuanceur pour des raisons pratiques.

L’exemple suivant illustre l’instruction **breakc** .


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Cette instruction doit apparaître dans une **boucle** / **ENDLOOP** ou **switch** / **endswitch**.

Le registre 32 bits fourni par *src0* est testé à un niveau binaire. Si un bit est différent de zéro, **breakc \_ NZ** effectuera l’arrêt. Si tous les bits sont nuls, **breakc \_ z** effectue l’arrêt.

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

 

 





