---
description: L’utilisation est similaire à la portée d’un paramètre, car elle définit la portée dans laquelle le paramètre est valide.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Utilisations et littéraux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513299"
---
# <a name="usages-and-literals-direct3d-9"></a>Utilisations et littéraux (Direct3D 9)

L’utilisation est similaire à la portée d’un paramètre, car elle définit la portée dans laquelle le paramètre est valide.



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valeur  | Description                                                                                                                                                                                                                                                                         |
| const  | Le paramètre sera constant dans la portée de toutes les fonctions. (Notez que ces paramètres peuvent toujours être écrits avec [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), car cela se produit en dehors de l’étendue de toutes les fonctions.) |
| partagés | Le paramètre sera partagé dans le pool d’effets.                                                                                                                                                                                                                                    |
| static | Le paramètre sera invisible pour l’application, autrement dit, vous ne pouvez pas y accéder à partir de [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).                                                                                                  |



 

Le marquage d’un paramètre en tant que littéral indique que sa valeur ne changera jamais. Cela permet au compilateur d’effet d’effectuer une optimisation supplémentaire.

Seuls les paramètres de niveau supérieur non partagés peuvent être marqués comme Literal. Les paramètres peuvent uniquement être marqués comme Literal avec [**ID3DXEffectCompiler**](id3dxeffectcompiler.md). Les valeurs littérales ne peuvent pas être définies avec [**ID3DXEffect**](id3dxeffect.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



