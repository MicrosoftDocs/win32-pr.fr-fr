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
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404157"
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

## <a name="remarks"></a>Notes

Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **getNextSelectedItem** , qui ne peut pas. Passe 1 dans le paramètre *Item* pour rechercher le premier élément sélectionné. Si aucun autre élément n’est sélectionné,-1 est retourné.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





