---
title: dcl_resource brut (SM5-ASM)
description: Déclarez une entrée de ressource de nuanceur et affectez-la à un registre d’espace réservé t \ a pour la ressource. | dcl_resource brut (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232523"
---
# <a name="dcl_resource-raw-sm5---asm"></a>DCL \_ ressource brute (SM5-ASM)

Déclarez une entrée de ressource de nuanceur et affectez-la à un \# Registre d’espace réservé t-a pour la ressource.



| \_ \_ dstSRV brute de la ressource DCL |
|---------------------------|



 



| Élément                                                                                           | Description                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[dans \] un \# Registre t déclaré comme référence à un ShaderResourceView d’une mémoire tampon brute.<br/> |



 

## <a name="remarks"></a>Notes

Le contenu de la structure n’a pas de type ; les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.

Les instructions qui font référence à un t brut \# acceptent une adresse 1D, une valeur non signée 32 bits qui spécifie l’offset d’octet à un emplacement aligné sur 32 bits dans la mémoire tampon. L’adresse doit être un multiple de 4 (octets).

Les vues liées à t \# déclarées comme RAW doivent avoir une valeur RAW spécifiée lors de leur création ; sinon, le comportement en cas d’accès à partir d’un nuanceur n’est pas défini.

CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
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

 

 





