---
title: PLAYLIST. getNextCheckedItem
description: La méthode getNextCheckedItem récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST. getNextCheckedItem Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54b6e598737d1aac09754b15c037c27a435deb5fff34c729aa48c51019e12982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571449"
---
# <a name="playlistgetnextcheckeditem"></a>PLAYLIST. getNextCheckedItem

La méthode **getNextCheckedItem** récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*fiche*
</dt> <dd>

**Nombre** (**long**) indiquant l’index de l’élément à rechercher après.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Notes

Lorsqu’il n’y a plus d’éléments activés, cette méthode retourne 1.

Cette méthode a été remplacée par **getNextCheckedItem2**, qui prend en charge les sélections imbriquées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





