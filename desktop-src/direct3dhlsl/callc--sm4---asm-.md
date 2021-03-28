---
title: callc (SM4-ASM)
description: Appelle de manière conditionnelle une sous-routine marquée par où l’étiquette l \ apparaît dans le programme.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990760"
---
# <a name="callc-sm4---asm"></a>callc (SM4-ASM)

Appelle de manière conditionnelle une sous-routine marquée par où l’étiquette **l \#** apparaît dans le programme.



| callc { \_ z \|\_NZ} src0. Sélectionnez le \_ composant, l\# |
|----------------------------------------------|



 



| Élément                                                            | Description                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le composant sur lequel tester la condition.<br/> |
| <span id="l_"></span><span id="L_"></span>*budget\#*<br/>      | \[dans \] l’étiquette de la sous-routine.<br/>                  |



 

## <a name="remarks"></a>Notes

Quand un [RET](ret--sm4---asm-.md) est rencontré, retourne l’exécution à l’instruction après cet appel.

Le format de jeton contient le décalage de l’étiquette correspondante dans le nuanceur pour des raisons pratiques.

L’exemple suivant illustre l’instruction call.


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a>Restrictions

-   Les sous-routines peuvent imbriquer 32 en profondeur.
-   La pile d’adresses de retour est gérée de façon transparente par l’implémentation de.
-   S’il existe déjà 32 entrées sur la pile d’adresses de retour et qu’un **appel** est émis, l’appel est ignoré.
-   Il n’existe pas de pile de paramètres automatique. L’application peut utiliser un tableau de registres temporaire indexable (x \# \[ \] ) pour implémenter manuellement une pile. Toutefois, les adresses de retour d’appel de sous-routine ne sont pas visibles et sont orthogonales à toute gestion de pile manuelle effectuée par l’application.
-   L’indexation du paramètre *l \#* n’est pas autorisée.
-   Le registre 32 bits fourni par *src0* est testé à un niveau binaire. Si un bit est différent de zéro, **callc \_ NZ** effectue l’appel. Si tous les bits sont nuls, **callc \_ z** effectue l’appel.
-   La récursivité n’est pas autorisée.

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

 

 





