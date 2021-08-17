---
title: dcl_temps (SM4-ASM)
description: DCL \_ temps (SM4-ASM)
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6426caff8ecd347ce8233f15df6b914a53c647ae79fb50a530b531e9207bf1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726807"
---
# <a name="dcl_temps-sm4---asm"></a>DCL \_ temps (SM4-ASM)

Déclare des registres temporaires.



| DCL- \_ temps N |
|--------------|



 



| Élément                                                   | Description                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[dans \] le nombre de registres temporaires.<br/> |



 

Chaque registre dispose d’espace pour une valeur de quatre composants de 32 bits. Le nombre total de registres temporaires et [indexables-temporaires](dcl-indexabletemp.md) doit être inférieur ou égal à 4096.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici un exemple.


```
dcl_temps 10; // Declare r0-r9
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

 

 





