---
title: Controls. currentItem
description: La propriété currentItem spécifie ou récupère l’élément multimédia actuel.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- controls. currentItem Lecteur Windows Media
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919360"
---
# <a name="controlscurrentitem"></a>Controls. currentItem

La propriété **CurrentItem** spécifie ou récupère l’élément multimédia actuel.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet **multimédia** en lecture/écriture.

## <a name="remarks"></a>Notes

Cette méthode fonctionne uniquement avec les éléments dans *Player*. **currentPlaylist**. L’appel de **CurrentItem** avec une référence à un élément multimédia enregistré n’est pas pris en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise **currentItem** pour définir l’élément multimédia actuel du contrôle de lecteur sur la valeur sélectionnée dans un élément SELECT HTML. La sélection actuelle a été spécifiée pour la première fois à l’aide de *PlaylistCollection*. **GetByName**. L’objet **Player** a été créé avec ID = "Player".


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





