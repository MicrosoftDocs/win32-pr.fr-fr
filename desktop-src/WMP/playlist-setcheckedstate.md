---
title: PLAYLIST. setCheckedState
description: La méthode setCheckedState spécifie que l’élément indexé dans la sélection est coché.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST. setCheckedState Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292970"
---
# <a name="playlistsetcheckedstate"></a>PLAYLIST. setCheckedState

La méthode **setCheckedState** spécifie que l’élément indexé dans la sélection est coché.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*fiche*
</dt> <dd>

**Nombre** (**long**) indiquant l’index de l’élément de sélection à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne une **valeur booléenne**.

## <a name="remarks"></a>Notes

Vous pouvez définir tous les éléments à l’état activé en spécifiant 1 dans le paramètre *Item* .

Cette méthode a été remplacée par **setCheckedState2**, qui prend en charge les sélections imbriquées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





