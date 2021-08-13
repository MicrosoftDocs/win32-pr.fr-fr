---
title: PLAYLIST. getNextSelectedItem
description: La méthode getNextSelectedItem récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- PLAYLIST. getNextSelectedItem Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 872dd31694384dfa35d7ce98c2f26756ede14539f4e788cbb6f699d17ca78a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467749"
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

## <a name="remarks"></a>Remarques

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

 

 





