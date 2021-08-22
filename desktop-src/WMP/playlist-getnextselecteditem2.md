---
title: PLAYLIST. getNextSelectedItem2
description: La méthode getNextSelectedItem2 récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST. getNextSelectedItem2 Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6d1f98a418da1d8b21345598999f847cbf2142e9ca575bcfdc7047e2f9fd524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415279"
---
# <a name="playlistgetnextselecteditem2"></a>PLAYLIST. getNextSelectedItem2

La méthode **getNextSelectedItem2** récupère l’index du prochain élément sélectionné dans la liste de sélection à la suite de l’index spécifié.

``` syntax
        elementID.getNextSelectedItem2(item)
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

Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **getNextSelectedItem** , qui ne peut pas. Passe 1 dans le paramètre *Item* pour rechercher le premier élément sélectionné. Si aucun autre élément n’est sélectionné,-1 est retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





