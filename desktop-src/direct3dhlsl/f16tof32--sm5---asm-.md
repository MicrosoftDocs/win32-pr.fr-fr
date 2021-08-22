---
title: f16tof32 (SM5-ASM)
description: Conversion float16 à float32 au niveau du composant. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc4456737d5ddaaed351ae2a1cc76418c33af9c498e725099e1912d8fabe7ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562650"
---
# <a name="f16tof32-sm5---asm"></a>f16tof32 (SM5-ASM)

Conversion float16 à float32 au niveau du composant.



| f16tof32 dest \[ . Mask \] , \[ - \] src \[ . Swizzle\] |
|----------------------------------------------|



 



| Élément                                                            | Description                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat float32.<br/> |
| <span id="src"></span><span id="SRC"></span>*sources*<br/>    | \[dans \] la valeur float16 à convertir.<br/>      |



 

## <a name="remarks"></a>Remarques

Cette opération effectue une conversion au niveau du composant d’une valeur float16 de LSB bits en un résultat float32.

Cette opération suit les règles D3D pour la conversion à virgule flottante.

Utilisez cette instruction pour la décompression des données pilotées par un nuanceur.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





