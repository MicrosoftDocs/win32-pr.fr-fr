---
title: 'Texture2DArray :: Texture2DArray, méthodes de regroupement'
description: Échantillonne un Texture2DArray et retourne les quatre composants.
ms.assetid: eea1dd00-0061-4601-a218-979eb0ecd36d
keywords:
- Méthodes de collecte HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 4b973060e30385087c653e47c692ac4d44e3eb63f528eb4e6f2ced65431100c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485209"
---
# <a name="texture2darraygather-methods"></a>Texture2DArray :: Gather, méthodes

Retourne les quatre valeurs de Texel d’un [**Texture2DArray**](sm5-object-texture2darray.md) qui seraient utilisées dans une opération de filtrage bilinéaire.

Pour plus d’informations sur la description de l’instruction DXBC sous-jacente, consultez la documentation sur [gather4](./gather4--sm5---asm-.md) .

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                | Description                                                                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**Gather (S, float, int)**](sm5-object-texture2darray-gather.md)        | Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.<br/>                                 |
| [**Gather (S, float, int, uint)**](t2darray-gather-s-float-int-uint-.md)  | Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> </dl>

 

