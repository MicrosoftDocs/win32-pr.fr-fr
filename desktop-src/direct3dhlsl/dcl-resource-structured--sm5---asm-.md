---
title: dcl_resource structuré (SM5-ASM)
description: Déclarez une entrée de ressource de nuanceur et affectez-la à un registre d’espace réservé t \ a pour la ressource. | dcl_resource structuré (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211429"
---
# <a name="dcl_resource-structured-sm5---asm"></a>\_ressource DCL structurée (SM5-ASM)

Déclarez une entrée de ressource de nuanceur et affectez-la à un \# Registre d’espace réservé t-a pour la ressource.



| \_ \_ dstSRV structurée des ressources DCL, structByteStride |
|----------------------------------------------------|



 



| Élément                                                                                                                                   | Description                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[dans \] un \# Registre t déclaré comme référence à un ShaderResourceView d’une mémoire tampon structurée avec la valeur Stride spécifiée qui doit être liée à \# l’emplacement SRV au niveau de l’API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[dans \] un uint qui spécifie la taille de la structure en octets dans la mémoire tampon en cours de déclaration. Cette valeur doit être supérieure à zéro.<br/>                                   |



 

## <a name="remarks"></a>Notes

Le contenu de la structure n’a pas de type ; les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.

Les instructions qui font référence à un t structuré \# acceptent une adresse 2D, où le premier composant choisit la \[ structure \] , et le deuxième composant choisit le \[ décalage dans le struct, multiple de 32 bits \] .

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction.

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

 

 





