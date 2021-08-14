---
title: PLAYLIST. setSelectedState2
description: La méthode setSelectedState2 définit l’état sélectionné de l’élément avec l’index spécifié dans l’élément PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST. setSelectedState2 Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f952d00486fe2419ab48592c7624299ef466c5dfa2b96d53fefb308fc537488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335811"
---
# <a name="playlistsetselectedstate2"></a>PLAYLIST. setSelectedState2

La méthode **setSelectedState2** définit l’état sélectionné de l’élément avec l’index spécifié dans l’élément **playlist** .

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*fiche*
</dt> <dd>

**Nombre** (**long**) indiquant l’index d’un élément dans la sélection.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*sélectionné*
</dt> <dd>

**Valeur booléenne** indiquant si l’élément spécifié doit être sélectionné (true) ou non sélectionné (false).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **setSelectedState** qui ne le peut pas. Vous pouvez définir tous les éléments à l’État demandé en spécifiant 1 dans le paramètre *Item* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setSelectedState**](playlist-setselectedstate.md)
</dt> </dl>

 

 





