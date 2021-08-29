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
ms.openlocfilehash: 1ba35f2030f4b2fb6e9acfde1a8310e6c9f1dac98b8ba8aa65d56cce206c8e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862239"
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

## <a name="remarks"></a>Remarques

Vous pouvez définir tous les éléments à l’état sélectionné en spécifiant 1 dans le paramètre *Item* .

Cette méthode a été remplacée par **setSelectedState2**, qui prend en charge les sélections imbriquées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





