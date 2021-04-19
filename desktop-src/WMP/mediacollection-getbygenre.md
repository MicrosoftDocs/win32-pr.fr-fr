---
title: Méthode MediaCollection. getByGenre
description: La méthode getByGenre récupère une sélection des éléments multimédias avec le genre spécifié.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- méthode getByGenre lecteur Windows Media
- méthode getByGenre lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537467"
---
# <a name="mediacollectiongetbygenre-method"></a>Méthode MediaCollection. getByGenre

La méthode **getByGenre** récupère une sélection des éléments multimédias avec le genre spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*genre* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom du genre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *MediaCollection*. **getByGenre** pour récupérer une sélection d’éléments multimédias. La sélection contient des éléments dont le genre est spécifié par l’utilisateur dans un élément d’entrée de texte HTML nommé GetGenre. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
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

 

 





