---
title: 'Texture2D :: Texture2D GatherCmp, méthodes'
description: Échantillonne et compare un Texture2D et retourne tous les composants.
ms.assetid: d520b113-77af-486e-8d3d-8276f72df18f
keywords:
- Méthodes GatherCmp HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 3a6c77cfc8215c3428f32204881acfea8990226f45283f30ec321bba99d773df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722926"
---
# <a name="texture2dgathercmp-methods"></a>Texture2D :: GatherCmp, méthodes

Pour quatre valeurs de Texel d’un [**Texture2D**](sm5-object-texture2d.md) qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.

Pour plus d’informations sur la description de l’instruction DXBC sous-jacente, consultez la documentation sur [gather4_c](./gather4-c--sm5---asm-.md) .

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                             | Description                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GatherCmp (S, float, float, int)**](sm5-object-texture2d-gathercmp.md)             | Échantillonne et compare une texture et retourne les quatre composants.<br/>                                       |
| [**GatherCmp (S, float, float, int, uint)**](t2d-gathercmp-s-float-float-int-uint-.md) | Échantillonne et compare une texture et retourne les quatre composants, ainsi que l’état de l’opération.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> </dl>

 

