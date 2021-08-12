---
title: Méthode MediaCollection. getByAlbum
description: La méthode GetByAlbum récupère une sélection contenant les éléments multimédias de l’album spécifié.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- Lecteur Windows Media de la méthode getByAlbum
- méthode getByAlbum Lecteur Windows Media, classe MediaCollection
- Lecteur Windows Media de la classe MediaCollection, méthode getByAlbum
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c17b7113b66f49822bad5586033312c9ec50711e6290c3f655a0a1b75adc54c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574672"
---
# <a name="mediacollectiongetbyalbum-method"></a>Méthode MediaCollection. getByAlbum

La méthode **GetByAlbum** récupère une sélection contenant les éléments multimédias de l’album spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*album* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’album.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise *MediaCollection*. **getByAlbum** pour récupérer une sélection d’éléments multimédias. La sélection contient des éléments avec l’album spécifié par l’utilisateur dans un élément d’entrée de texte HTML nommé GetAlbum. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





