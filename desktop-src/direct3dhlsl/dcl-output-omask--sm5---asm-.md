---
title: dcl_output oMask (SM5-ASM)
description: Déclarez un registre de sortie à écrire par le nuanceur.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a6860904b557bc21a5202bbfd60105852adc260580457afb02b4fe6d92352b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068509"
---
# <a name="dcl_output-omask-sm5---asm"></a>\_oMask de sortie DCL (SM5-ASM)

Déclarez un registre de sortie à écrire par le nuanceur.



| la \_ sortie DCL o \# \[ . Mask\] |
|--------------------------|



 



| Élément                                                   | Description                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*sorties*<br/> | \[dans \] le registre de sortie.<br/> |



 

## <a name="remarks"></a>Remarques


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Restrictions

-   Le masque de composant peut être n’importe quel sous-ensemble de \[ XYZW \] . Toutefois, laisser des écarts entre les composants gaspille de l’espace.
-   Il est légal de déclarer un sur-ensemble du masque de composant déclaré pour l’entrée à l’étape suivante. Toutefois, les masques mutuellement exclusifs ne sont pas autorisés. Le nuanceur de sommets, à partir de O3. XY, signifie que le nuanceur de pixels qui entre v3. z n’est pas valide, mais où v3. x ou v3. y ou v3. XY est valide.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





