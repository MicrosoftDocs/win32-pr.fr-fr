---
title: 'Texture2DArray :: Texture2DArray GatherCmp, méthodes'
description: Échantillonne et compare un Texture2DArray et retourne tous les composants.
ms.assetid: 5b2892f0-be62-4fb2-978e-aabb8ae96e67
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
ms.openlocfilehash: 760c6313df2fb50ea821495d9f57933aef5bb0cc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973891"
---
# <a name="texture2darraygathercmp-methods"></a>Texture2DArray :: GatherCmp, méthodes

Pour quatre valeurs de Texel d’un [**Texture2DArray**](sm5-object-texture2darray.md) qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.

Pour plus d’informations sur la description de l’instruction DXBC sous-jacente, consultez la documentation sur [gather4_c](./gather4-c--sm5---asm-.md) .

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                             | Description                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GatherCmp (S, float, float, int)**](sm5-object-texture2darray-gathercmp.md)        | Échantillonne et compare une texture et retourne les quatre composants.<br/>                                       |
| [**GatherCmp (S, float, float, int, uint)**](t2d-gathercmp-s-float-float-int-uint-.md) | Échantillonne et compare une texture et retourne les quatre composants, ainsi que l’état de l’opération.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> </dl>

 

