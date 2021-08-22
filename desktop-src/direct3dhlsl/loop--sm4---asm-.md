---
title: boucle (SM4-ASM)
description: Spécifie une boucle qui itère jusqu’à ce qu’une instruction Break soit rencontrée.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dfc3090e71c1101e2c2748924de24f5443363ede76b86130cf63c3a319c76ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043767"
---
# <a name="loop-sm4---asm"></a>boucle (SM4-ASM)

Spécifie une boucle qui itère jusqu’à ce qu’une instruction Break soit rencontrée.



| loop |
|------|



 

## <a name="remarks"></a>Remarques

**Loop** peut itérer indéfiniment, bien que l’exécution globale du nuanceur puisse être forcée à se terminer après l’exécution d’un certain nombre d’instructions.

les blocs de contrôle Flow peuvent s’imbriquer jusqu’à 64 de profondeur par sous-routine et main. Le compilateur HLSL ne génère pas de sous-routines qui dépassent cette limite. Le comportement des instructions de workflow de contrôle au-delà de 64 niveaux de profondeur par sous-routine n’est pas défini.

Le format de jeton contient le décalage de l’instruction [ENDLOOP](endloop--sm4---asm-.md) correspondante dans le nuanceur pour des raisons pratiques.

L’exemple suivant montre comment utiliser l’instruction de boucle.

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

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

 

 




