---
title: uaddc (SM5-ASM)
description: Entier non signé ajouter avec Carry.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f649ed68626e5b3351ee1b3c7d5848c8e42f7ec175b4b76c929571056f48e0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722187"
---
# <a name="uaddc-sm5---asm"></a>uaddc (SM5-ASM)

Entier non signé ajouter avec Carry.



| uaddc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Élément                                                               | Description                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[dans \] adresse du résultat.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[en \] 1 si le transport est produit. Sinon, 0.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[dans l' \] opérande 32 bits à ajouter.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[dans l' \] opérande 32 bits à ajouter.<br/>          |



 

## <a name="remarks"></a>Remarques

*dest1* peut avoir la valeur null si le transport n’est pas nécessaire.

Utilisez cette instruction pour les opérations arithmétiques de haute précision.

Cette instruction s’applique aux étapes suivantes du nuanceur :



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



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





