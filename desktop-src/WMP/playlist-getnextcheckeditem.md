---
title: PLAYLIST. getNextCheckedItem
description: La méthode getNextCheckedItem récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Lecteur Windows Media PLAYLIST. getNextCheckedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532920"
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

 

 





