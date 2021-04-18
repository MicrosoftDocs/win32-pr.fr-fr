---
title: Player. currentPlaylist
description: La propriété currentPlaylist spécifie ou récupère l’objet de sélection actuel.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Lecteur Windows Media Player. currentPlaylist
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526811"
---
# <a name="playercurrentplaylist"></a>Player. currentPlaylist

La propriété currentPlaylist spécifie ou récupère l’objet de **sélection** actuel.

## <a name="syntax"></a>Syntaxe

*lecteur* . **currentPlaylist**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet de **sélection** en lecture/écriture.

## <a name="remarks"></a>Notes

Si les *paramètres*. la propriété **AutoStart** a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentPlaylist**.

Cette propriété prend un objet playlist, qui peut être acquis de plusieurs façons, par exemple en appelant *PlaylistArray*. **Item** ou *PlaylistCollection*. **newPlaylist**. Pour charger un élément de **sélection** à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez *Player*. **newPlaylist**.

## <a name="examples"></a>Exemples

L’exemple JScript suivant récupère la première sélection de la bibliothèque. Il utilise ensuite **currentPlaylist** pour faire de la sélection Récupérée la sélection actuelle, puis pour afficher le nom de la sélection actuelle. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistArray. Item**](playlistarray-item.md)
</dt> <dt>

[**PlaylistCollection. newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Paramètres. démarrage automatique**](settings-autostart.md)
</dt> </dl>

 

 





