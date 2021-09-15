---
title: dcl_uav_typed (SM5-ASM)
description: Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411250"
---
# <a name="dcl_uav_typed-sm5---asm"></a>DCL \_ UAV \_ typée (SM5-ASM)

Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur.



| DCL \_ UAV \_ typé \[ \_ GLC \] dstUAV, dimension, type |
|--------------------------------------------------|



 



| Élément                                                                                           | Description                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[dans \] le UAV.<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*codes*<br/>                 | \[dans \] spécifie le nombre de dimensions fournies par les instructions qui accèdent au UAV.<br/> |
| <span id="type"></span><span id="TYPE"></span>*entrer*<br/>                                | \[dans \] le type de UAV.<br/>                                                            |



 

## <a name="remarks"></a>Notes

*dstUAV* est un \# Registre u qui est déclaré en tant que référence à un UnorderedAccessView qui doit être lié à \# l’emplacement UAV au niveau de l’API.

La dimension doit être buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray ou Texture3D. Cela indique le nombre de dimensions fournies par toutes les instructions qui accèdent au UAV : 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) ou 3 (Texture2DArray, Texture3D).

Le type est {UNORM, RONFLEr, UINT, Saint, FLOAT}. Les opérations effectuées avec l’u déclaré \# doivent être compatibles avec le type déclaré ici, et la UAV liée à l’emplacement \# doit également avoir le même type.

L' \_ indicateur GLC signifie « cohérence globale ». L’absence de \_ GLC signifie que le UAV est déclaré comme « cohérent par le groupe » dans le nuanceur de calcul, ou « cohérent localement » dans un appel de nuanceur de pixel unique.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> Cette instruction n’est pas prise en charge dans le nuanceur de calcul 4. x.

 

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

 

 





