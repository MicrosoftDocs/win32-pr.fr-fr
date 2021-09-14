---
title: PLAYLIST. setCheckedState2
description: La méthode setCheckedState2 définit l’état activé de l’élément avec l’index spécifié dans l’élément PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST. setCheckedState2 Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292967"
---
# <a name="playlistsetcheckedstate2"></a>PLAYLIST. setCheckedState2

La méthode **setCheckedState2** définit l’état activé de l’élément avec l’index spécifié dans l’élément **playlist** .

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*fiche*
</dt> <dd>

**Nombre** (**long**) indiquant l’index de l’élément de sélection à activer ou désactiver.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*désactivé*
</dt> <dd>

**Valeur booléenne** indiquant si l’élément spécifié doit être activé (true) ou désactivé (false).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne une **valeur booléenne**.

## <a name="remarks"></a>Notes

Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **setCheckedState** , qui ne peut pas. Vous pouvez définir tous les éléments à l’État demandé en spécifiant 1 dans le paramètre *Item* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





