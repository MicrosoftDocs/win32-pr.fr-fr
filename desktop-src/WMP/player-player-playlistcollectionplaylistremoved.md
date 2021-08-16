---
title: Événement Player. PlaylistCollectionPlaylistRemoved
description: L’événement PlaylistCollectionPlaylistRemoved se produit lorsqu’une sélection est supprimée de la collection de sélections. | Événement Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Lecteur Windows Media d’événements PlaylistCollectionPlaylistRemoved
- Lecteur Windows Media d’événements PlaylistCollectionPlaylistRemoved, classe Player
- Lecteur Windows Media de classe Player, événement PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 456f7598b9e1f1d2c2a6e76e58a0b06142980835c3c6d71d9ab10c2230ac386f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118337973"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Événement Player. PlaylistCollectionPlaylistRemoved

L’événement **PlaylistCollectionPlaylistRemoved** se produit lorsqu’une sélection est supprimée de la collection de sélections.

## <a name="syntax"></a>Syntaxe


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Chaîne** spécifiant le nom de la sélection qui a été supprimée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





