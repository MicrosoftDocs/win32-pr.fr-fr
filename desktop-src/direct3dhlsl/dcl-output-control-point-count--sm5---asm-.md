---
title: dcl_output_control_point_count (SM5-ASM)
description: Déclare le nombre de points de contrôle de sortie du nuanceur de coque.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dc28a2af3ac50c835fa7ec38d7d344029af76a11cb2b84945dbf5009d68473
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024699"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>\_nombre de \_ \_ points de contrôle de sortie DCL \_ (SM5-ASM)

Déclare le nombre de points de contrôle de sortie du nuanceur de coque.



| \_nombre de points de contrôle de sortie DCL \_ \_ \_ N |
|--------------------------------------|



 



| Élément                                                   | Description                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[\]valeur entière comprise entre 0 et 32 qui spécifie le nombre de points de contrôle de sortie.<br/> |



 

## <a name="remarks"></a>Remarques

Le nuanceur de coque peut générer des points de contrôle 0 s’ils ne sont pas nécessaires.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme                 | Domaine | Géométrie | Pixel | Calcul |
|--------|----------------------|--------|----------|-------|---------|
|        | Section déclarations |        |          |       |         |



 

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

 

 





