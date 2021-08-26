---
title: PLAYLIST. copier
description: La méthode de copie commence une opération de copie à partir du CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- PLAYLIST. copy Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b897d22c1aa8e666c5de40aecb8ef63d17384957e82eee8dc7d569f0e71f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003189"
---
# <a name="playlistcopy"></a>PLAYLIST. copier

La méthode de **copie** commence une opération de copie à partir du CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

cette méthode copie uniquement les éléments cochés dans la sélection et fonctionne de la même façon que dans le volet **copier à partir du CD** en mode complet de Lecteur Windows Media. Pour que cette méthode fonctionne, un CD doit se trouver dans le lecteur de CD. Affectez la valeur true à l’attribut **checkboxesVisible** pour permettre aux utilisateurs de sélectionner des éléments individuels sur un CD avant la copie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**PLAYLIST. copie**](playlist-copying.md)
</dt> </dl>

 

 





