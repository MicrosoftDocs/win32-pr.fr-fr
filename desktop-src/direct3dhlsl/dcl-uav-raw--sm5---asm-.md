---
title: dcl_uav_raw (SM5-ASM)
description: Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b7af99a1747d23d6269ffc1b7199fb142277b46e73bfd822d31fd4b0fbf3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986689"
---
# <a name="dcl_uav_raw-sm5---asm"></a>DCL \_ UAV \_ brute (SM5-ASM)

Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur.



| DCL \_ UAV \_ brute \[ \_ GLC \] dstUAV |
|-------------------------------|



 



| Élément                                                                                           | Description                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[dans \] le UAV.<br/> |



 

## <a name="remarks"></a>Remarques

*dstUAV* est un \# Registre u déclaré comme référence à un UnorderedAccessView d’une mémoire tampon, où la mémoire tampon apparaît sous la forme d’un tableau 1D simple d’entrées non typées 32 bits.

Les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.

L' \_ indicateur GLC signifie « cohérence globale ». L’absence de \_ GLC signifie que le UAV est déclaré comme « cohérent par le groupe » dans le nuanceur de calcul, ou « cohérent localement » dans un appel de nuanceur de pixel unique.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



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



 

> [!Note]  
> Cette instruction est prise en charge dans cs \_ 4 \_ 0 et CS \_ 4 \_ 1.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





