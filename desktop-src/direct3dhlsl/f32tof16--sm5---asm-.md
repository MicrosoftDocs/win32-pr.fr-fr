---
title: f32tof16 (SM5-ASM)
description: Conversion float16 à float32 au niveau du composant. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974398"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (SM5-ASM)

Conversion float16 à float32 au niveau du composant.



| f32tof16 dest \[ . Mask \] , \[ - \] src \[ . Swizzle\] |
|----------------------------------------------|



 



| Élément                                                            | Description                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] l’adresse du résultat de float16.<br/> |
| <span id="src"></span><span id="SRC"></span>*sources*<br/>    | \[dans \] la valeur float32 à convertir.<br/>  |



 

## <a name="remarks"></a>Notes

Cette instruction effectue une conversion au niveau du composant d’une valeur float32 en un résultat de valeur float16 placé dans le LSB 16 bits.

Cette instruction suit les règles D3D pour la conversion à virgule flottante.

Utilisez cette instruction pour la compression des données pilotées par un nuanceur.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





