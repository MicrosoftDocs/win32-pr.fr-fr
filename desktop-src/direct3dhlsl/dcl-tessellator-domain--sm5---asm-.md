---
title: dcl_tessellator_domain (SM5-ASM)
description: Déclarez le domaine du paveur dans une section de déclaration de nuanceur de coque et le nuanceur de domaine.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a027e9fab091cf31e8577266015e974ec78033fe19a9542f0aa3c6ca4651db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986709"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>\_domaine du paveur DCL \_ (SM5-ASM)

Déclarez le domaine du paveur dans une section de déclaration de nuanceur de coque et le nuanceur de domaine.



| DCL \_ du paveur \_ domaine {domaine \_ isoligne \| domaine \_ Tri \| domaine \_ Quad} |
|---------------------------------------------------------------------------|



 



| Élément                                                                                                                                                                                | Description                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*Domain \_ isoligne Domain tri domaine- \| \_ \| \_ Quad*<br/> | \[dans \] le domaine.<br/> |



 

## <a name="remarks"></a>Remarques

Le comportement n’est pas défini si le nuanceur de coque et le nuanceur de domaine fournissent des domaines incompatibles ou tout autre decalarations en conflit.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme                 | Domaine | Géométrie | Pixel | Calcul |
|--------|----------------------|--------|----------|-------|---------|
|        | Section déclarations | X      |          |       |         |



 

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

 

 





