---
title: dcl_indexableTemp (SM4-ASM)
description: DCL \_ indexableTemp (SM4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f1d6e02b36daef0643910d69404adc0973ebbcf6370ae5f5c11ad2aa7bd3480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793445"
---
# <a name="dcl_indexabletemp-sm4---asm"></a>DCL \_ indexableTemp (SM4-ASM)

Déclare un registre temporaire indexé.



| DCL \_ indexableTemp x *N \[ taille \] , ComponentCount* |
|-------------------------------------------------|



 



| Élément                                                                                                                           | Description                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/>                                                                         | \[dans \] un entier qui indique le numéro du Registre.<br/>                              |
| <span id="_size_"></span><span id="_SIZE_"></span>*\[corps\]*<br/>                                                        | \[dans \] une valeur entière facultative. Nombre d’éléments dans le tableau de registres.<br/>  |
| <span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*<br/> | \[dans \] une valeur entière facultative. Nombre de composants dans le tableau de registres.<br/> |



 

Un registre contient suffisamment d’espace pour une valeur de quatre composants 32 bits ; le nombre d’éléments dans le tableau de registres temporaires (indexable et [non indexable](dcl-temps.md)) ne peut pas dépasser 4096.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a> Exemple

Voici quelques exemples du code généré pour les registres indexables.


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



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

 

 





