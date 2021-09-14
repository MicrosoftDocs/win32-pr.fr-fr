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
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293030"
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

## <a name="remarks"></a>Notes

cette méthode copie uniquement les éléments cochés dans la sélection et fonctionne de la même façon que dans le volet **copier à partir du CD** en mode complet de Lecteur Windows Media. Pour que cette méthode fonctionne, un CD doit se trouver dans le lecteur de CD. Affectez la valeur true à l’attribut **checkboxesVisible** pour permettre aux utilisateurs de sélectionner des éléments individuels sur un CD avant la copie.

## <a name="requirements"></a>Spécifications



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

 

 





