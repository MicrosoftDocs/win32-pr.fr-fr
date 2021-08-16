---
title: dcl_uav_structured (SM5-ASM)
description: Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b398dc8b59db6d8fc3a64effdf3cd93b56664881c4c7024a185ad6a212b9fb4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726797"
---
# <a name="dcl_uav_structured-sm5---asm"></a>DCL \_ UAV \_ structurée (SM5-ASM)

Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur.



| DCL \_ UAV \_ structuré \[ \_ GLC \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Élément                                                                                                                                   | Description                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[dans \] le UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[dans \] la taille de la structure en octets.<br/> |



 

## <a name="remarks"></a>Remarques

*dstUAV* est un \# Registre u déclaré comme référence à un UnorderedAccessView d’une mémoire tampon structurée avec la valeur Stride spécifiée qui doit être liée à \# l’emplacement UAV au niveau de l’API.

Le contenu de la structure n’a pas de type ; les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.

*structByteStride* est la taille de la structure en octets dans la mémoire tampon en cours de déclaration. Cette valeur doit être supérieure à zéro. *structByteStride* est de type uint et doit être un multiple de 4.

Les instructions qui font référence à un u structuré \# prennent une adresse 2D, où le premier composant sélectionne la \[ structure \] , et le deuxième composant choisit le décalage dans la \[ structure, en octets alignés \] .

L' \_ indicateur GLC signifie « cohérence globale ». L’absence de \_ GLC signifie que le UAV est déclaré comme « cohérent par le groupe » dans le nuanceur de calcul, ou « cohérent localement » dans un appel de nuanceur de pixel unique.

L' \_ indicateur OPC est le compteur de préservation de l’ordre. Elle indique que si un UAV est lié à \# l’emplacement (u \# ), il doit avoir été créé avec l’indicateur de compteur. Cela signifie que les opérations d' [ \_ \_ allocation atomique](imm-atomic-alloc--sm5---asm-.md) d’un IMM ou d’un IMM dans le nuanceur manipulent un compteur dont les valeurs peuvent être utilisées dans le nuanceur en tant que référence permanente à un emplacement dans le UAV. [ \_ \_ ](imm-atomic-consume--sm5---asm-.md) Les données ne peuvent pas être réorganisées après le dépassement du nuanceur.

L’absence de l' \_ indicateur OPC signifie que si le nuanceur utilise des instructions[IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) et qu’un UAV est lié à l’emplacement \# (u), il doit avoir été créé avec l’indicateur Append, qui fournit un compteur qui ne garantit pas que l’ordre est conservé après l’appel du nuanceur.

Si l' \_ indicateur OPC est absent et que le nuanceur ne contient pas d’instructions [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou [IMM \_ Atomic \_ Consumer](imm-atomic-consume--sm5---asm-.md) , une UAV liée à \# l’emplacement (u) est autorisée à avoir été créée avec l’indicateur de compteur (le compteur sera inutilisé par ce nuanceur), aucun indicateur (aucun compteur), mais pas avec l’indicateur Append.

> [!Note]  
> CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge la **\_ TGSM \_ structurée DCL**, mais pas la [ \_ TGSM \_ brute du DCL](dcl-tgsm-raw--sm5---asm-.md).

 

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

 

 





