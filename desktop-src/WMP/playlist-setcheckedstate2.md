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
ms.openlocfilehash: b6b95cb332c5f5a9d86e6f49484b27c1ab5802f28b18195f610395a1c732e369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336218"
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

## <a name="remarks"></a>Remarques

Cette méthode peut fonctionner avec des sélections imbriquées et remplace la méthode **setCheckedState** , qui ne peut pas. Vous pouvez définir tous les éléments à l’État demandé en spécifiant 1 dans le paramètre *Item* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





