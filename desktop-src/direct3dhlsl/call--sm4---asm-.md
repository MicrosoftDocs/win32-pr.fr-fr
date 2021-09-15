---
title: appel (SM4-ASM)
description: Appelle une sous-routine marquée par où l’étiquette l \ apparaît dans le programme.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524860"
---
# <a name="call-sm4---asm"></a>appel (SM4-ASM)

Appelle une sous-routine marquée par l’emplacement où l’étiquette **l \#** apparaît dans le programme.



| appeler l\# |
|----------|



 



| Élément                                                       | Description                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*budget\#*<br/> | \[dans \] l’étiquette de la sous-routine.<br/> |



 

## <a name="remarks"></a>Notes

Quand un [RET](ret--sm4---asm-.md) est rencontré, retourne l’exécution à l’instruction après cet appel.

Le format de jeton contient le décalage de l’étiquette correspondante dans le nuanceur pour des raisons pratiques.

L’exemple suivant illustre l’instruction call.


```
                ...
                call l3
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

 

 





