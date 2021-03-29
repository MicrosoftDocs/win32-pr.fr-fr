---
title: dcl_function_table (SM5-ASM)
description: Déclarez une table de fonctions.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990849"
---
# <a name="dcl_function_table-sm5---asm"></a>\_ \_ table de fonctions DCL (SM5-ASM)

Déclarez une table de fonctions.



| \_ \_ table de fonctions DCL ft \# = {FB \# , FB \# ,...} |
|-----------------------------------------------|



 



| Élément                                                      | Description                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*pied*<br/> | \[dans \] les entrées de la table de fonctions.<br/> |



 

## <a name="remarks"></a>Notes

Cette fonction déclare une table de fonctions comme un ensemble de corps de fonction qui ont été déclarés précédemment.

C’est comme une vtable C++, sauf qu’il existe une entrée par site d’appel pour une interface plutôt que par méthode.

Il n’existe aucune limite au nombre de corps de fonction qui peuvent être listés dans une table de fonctions.

Il est valide pour un corps de fonction en FB \# référencé à plusieurs moments dans une ou plusieurs tables de fonctions, comme un moyen de partager le code commun.

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

 

 





