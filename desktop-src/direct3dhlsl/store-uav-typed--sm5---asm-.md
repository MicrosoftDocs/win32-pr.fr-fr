---
title: store_uav_typed (SM5-ASM)
description: Écriture à accès aléatoire d’un élément dans une vue d’accès non triée typée (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922224"
---
# <a name="store_uav_typed-sm5---asm"></a>Store \_ UAV \_ typé (SM5-ASM)

Écriture à accès aléatoire d’un élément dans une vue d’accès non triée typée (UAV).



| Store \_ UAV \_ typé dstUAV. XYZW, dstAddress \[ . Swizzle \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------------------|



 



| Élément                                                                                                           | Description                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[dans \] contient le résultat de l’opération.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[dans \] l’adresse à laquelle écrire.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[dans \] les composants à écrire.<br/>              |



 

## <a name="remarks"></a>Notes

Cette instruction effectue un élément de 4 composants \* 32 bits écrit à partir de *Src0* vers *dstUAV* à l’adresse dans *dstAddress*. *dstUAV* est un UAV typé (u \# ).

Le format de UAV détermine la conversion de format.

Le nombre de composants entiers non signés 32 bits pris à partir de l’adresse est déterminé par la dimensionnalité de la ressource déclarée dans *dstUAV*. Cette adresse se trouve dans les éléments.

L’adressage hors limites signifie que rien n’est écrit dans la mémoire.

*dstUAV* a toujours un masque d’écriture. XYZW. Tous les composants doivent être écrits.

Il n’est pas valide et n’est pas défini pour utiliser cette instruction sur un UAV qui n’est pas déclaré comme typé. Autrement dit, cette action sur un UAV structuré ou non n’est pas valide.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.



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

 

 





