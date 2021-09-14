---
title: Événement Player. PlaylistCollectionPlaylistAdded
description: L’événement PlaylistCollectionPlaylistAdded se produit lorsqu’une sélection est ajoutée à la collection de sélections. | Événement Player. PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Lecteur Windows Media d’événements PlaylistCollectionPlaylistAdded
- Lecteur Windows Media d’événements PlaylistCollectionPlaylistAdded, classe Player
- Lecteur Windows Media de classe Player, événement PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292110"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Événement Player. PlaylistCollectionPlaylistAdded

L’événement **PlaylistCollectionPlaylistAdded** se produit lorsqu’une sélection est ajoutée à la collection de sélections.

## <a name="syntax"></a>Syntaxe


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Chaîne** spécifiant le nom de la sélection ajoutée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le nom de la sélection ajoutée peut être utilisé pour récupérer l’objet de **sélection** correspondant à l’aide de *PlaylistCollection*. méthode **GetByName** .

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



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

 

 





