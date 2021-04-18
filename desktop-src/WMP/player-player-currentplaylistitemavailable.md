---
title: Événement Player. CurrentPlaylistItemAvailable
description: L’événement CurrentPlaylistItemAvailable se produit lorsque la sélection actuelle est disponible. | Événement Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Événement CurrentPlaylistItemAvailable lecteur Windows Media
- Événement CurrentPlaylistItemAvailable lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540500"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Événement Player. CurrentPlaylistItemAvailable

L’événement **CurrentPlaylistItemAvailable** se produit lorsque la sélection actuelle est disponible.

## <a name="syntax"></a>Syntaxe


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Chaîne** contenant le nom de l’élément de sélection actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le nom de la sélection actuelle peut être utilisé pour récupérer l’objet de **sélection** correspondant à l’aide de *PlaylistCollection*. méthode **GetByName** .

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

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

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





