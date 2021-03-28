---
title: dcl_function_body (SM5-ASM)
description: Déclarez un corps de fonction.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101113"
---
# <a name="dcl_function_body-sm5---asm"></a>\_corps de la fonction DCL \_ (SM5-ASM)

Déclarez un corps de fonction.



| corps de la \_ fonction DCL \_ FB\# |
|--------------------------|



 



| Élément                                                          | Description                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*disposez\#*<br/> | \[dans \] l’étiquette de l’emplacement où la fonction apparaît.<br/> |



 

## <a name="remarks"></a>Notes

Cette instruction déclare un corps de fonction unique dont le code apparaîtra ultérieurement dans le programme à l’étiquette FB \# .

Les corps de fonction sont utilisés dans les déclarations de table de fonctions. Pour plus d’informations, [consultez \_ \_ table de fonctions DCL](dcl-function-table---sm5---asm-.md).

Dans le nuanceur de coque et le nuanceur de domaine, où il y a plusieurs phases (phase de point de contrôle, phase de branchement et phase de jointure), tous les corps de fonction (étiquette FB \# ) apparaissent après toutes les phases, au lieu d’être regroupés par phase.

Il n’existe aucune limite au nombre de corps de fonction qui peuvent être présents.

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

 

 





