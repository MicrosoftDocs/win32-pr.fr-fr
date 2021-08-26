---
title: ld_uav_typed (SM5-ASM)
description: Lecture à accès aléatoire d’un élément à partir d’une vue d’accès non triée typée (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9685341f4a3a2e6b22bbbcc4b36f6ecccc153f17c67f38c390e6beeef94358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982069"
---
# <a name="ld_uav_typed-sm5---asm"></a>LD \_ UAV \_ typé (SM5-ASM)

Lecture à accès aléatoire d’un élément à partir d’une vue d’accès non triée typée (UAV).



| LD \_ UAV \_ typé dst0 \[ . Mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Élément                                                                                                           | Description                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[dans \] l’adresse des résultats de l’opération.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[dans \] spécifie l’adresse à partir de laquelle effectuer la lecture.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[dans \] la source à lire. <br/>                    |



 

## <a name="remarks"></a>Remarques

Cette instruction effectue une lecture d’élément à 4 composants à partir de *srcUAV* à l’adresse entière non signée dans *srcAddress*, convertie en 32 bits par composant en fonction du format, puis écrite dans *dst0* dans le nuanceur.

*srcUAV* est un UAV (u \# ) déclaré comme typé. Toutefois, le type de la ressource liée doit être R32 \_ uint/Saint/.

Le nombre de composants entiers non signés 32 bits pris à partir de l’adresse est déterminé par la dimensionnalité de la ressource déclarée dans *srcUAV*. L’adressage est le même que l’instruction [LD](ld--sm4---asm-.md) .

L’adressage hors limites est le même que l’instruction **LD** .

Le comportement de cette instruction est identique à l’instruction **LD** si elle est appelée en tant que **LD dst0 \[ . Mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . Swizzle \]**

Il n’est pas valide et n’est pas défini pour utiliser cette instruction sur un UAV qui n’est pas déclaré comme typé. Le fait de procéder sur un UAV structuré ou non n’est pas valide.

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



 

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV, SRV et TGSM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





