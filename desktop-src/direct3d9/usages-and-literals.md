---
description: L’utilisation est similaire à la portée d’un paramètre, car elle définit la portée dans laquelle le paramètre est valide.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Utilisations et littéraux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8c9fa8eb30726e783ce763ec8700f715dbd5d2b85ff3bf98340cf604e8e2f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026009"
---
# <a name="usages-and-literals-direct3d-9"></a>Utilisations et littéraux (Direct3D 9)

L’utilisation est similaire à la portée d’un paramètre, car elle définit la portée dans laquelle le paramètre est valide.



| Valeur  | Description                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| const  | Le paramètre sera constant dans la portée de toutes les fonctions. (Notez que ces paramètres peuvent toujours être écrits avec [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), car cela se produit en dehors de l’étendue de toutes les fonctions.) |
| partagés | Le paramètre sera partagé dans le pool d’effets.                                                                                                                                                                                                                                    |
| static | Le paramètre sera invisible pour l’application, autrement dit, vous ne pouvez pas y accéder à partir de [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).                                                                                                  |



 

Le marquage d’un paramètre en tant que littéral indique que sa valeur ne changera jamais. Cela permet au compilateur d’effet d’effectuer une optimisation supplémentaire.

Seuls les paramètres de niveau supérieur non partagés peuvent être marqués comme Literal. Les paramètres peuvent uniquement être marqués comme Literal avec [**ID3DXEffectCompiler**](id3dxeffectcompiler.md). Les valeurs littérales ne peuvent pas être définies avec [**ID3DXEffect**](id3dxeffect.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



