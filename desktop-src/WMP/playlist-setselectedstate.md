---
title: PLAYLIST. setSelectedState
description: La méthode setSelectedState spécifie que l’élément indexé dans la sélection est sélectionné.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- PLAYLIST. setSelectedState Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292955"
---
# <a name="playlistsetselectedstate"></a>PLAYLIST. setSelectedState

La méthode **setSelectedState** spécifie que l’élément indexé dans la sélection est sélectionné.

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*fiche*
</dt> <dd>

**Nombre** (**long**) indiquant l’index d’un élément dans la sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Vous pouvez définir tous les éléments à l’état sélectionné en spécifiant 1 dans le paramètre *Item* .

Cette méthode a été remplacée par **setSelectedState2**, qui prend en charge les sélections imbriquées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





