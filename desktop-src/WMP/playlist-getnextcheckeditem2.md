---
title: PLAYLIST. getNextCheckedItem2
description: La méthode getNextCheckedItem2 récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST. getNextCheckedItem2 Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293010"
---
# <a name="playlistgetnextcheckeditem2"></a>PLAYLIST. getNextCheckedItem2

La méthode **getNextCheckedItem2** récupère l’index de l’élément activé suivant dans la playlist à la suite de l’index spécifié.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **getNextCheckedItem** , qui ne peut pas. Passe 1 dans le paramètre d' *élément* pour rechercher le premier élément activé. Lorsqu’il n’y a plus d’éléments activés, cette méthode retourne 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





