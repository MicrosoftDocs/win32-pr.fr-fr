---
title: PLAYLIST. getNextSelectedItem
description: La méthode getNextSelectedItem récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Lecteur Windows Media PLAYLIST. getNextSelectedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523879"
---
# <a name="playlistgetnextselecteditem"></a>PLAYLIST. getNextSelectedItem

La méthode **getNextSelectedItem** récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.

``` syntax
        elementID.getNextSelectedItem(item)
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

Si aucun autre élément n’est sélectionné, cette méthode retourne 1.

Cette méthode a été remplacée par **getNextSelectedItem2**, qui prend en charge les sélections imbriquées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





