---
title: dcl_output (SM4-ASM)
description: '\_sortie DCL (SM4-ASM)'
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d60f50250a3bf35056cd7232100fbac3e3d919c3c473436899e359f26f84ecea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726986"
---
# <a name="dcl_output-sm4---asm"></a>\_sortie DCL (SM4-ASM)

Déclare un registre Shader-output.



| \_sortie DCL o *N \[ . masque \]* |
|---------------------------|



 



| Élément                                                                           | Description                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/> | \[dans \] un registre de données de sortie ; *N* est un entier qui indique le numéro du Registre.<br/>               |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*<br/>     | \[\]facultatif. Masque de composant (. XYZW) qui spécifie les composants Register à utiliser.<br/> |



 

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici quelques exemples.


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
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

 

 





