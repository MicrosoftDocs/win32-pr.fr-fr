---
title: dcl_input_control_point_count (SM5-ASM)
description: Déclarez le nombre de points de contrôle d’entrée du nuanceur de coque dans la section Déclaration du nuanceur de coque.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381237"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>\_nombre de \_ points de contrôle d’entrée DCL \_ \_ (SM5-ASM)

Déclarez le nombre de points de contrôle d’entrée du nuanceur de coque dans la section Déclaration du nuanceur de coque.



| \_nombre de points de contrôle d’entrée DCL \_ \_ \_ {1.. 32} |
|-------------------------------------------|



 



| Élément                                                   | Description                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[dans \] le nombre de points de contrôle d’entrée.<br/> |



 

## <a name="remarks"></a>Notes

Au moins 1 point de contrôle d’entrée est requis ; Il peut être vide s’il n’est pas nécessaire.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

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

 

 





