---
title: Méthode MediaCollection. getByAuthor
description: La méthode getByAuthor récupère une sélection des éléments multimédias par l’auteur spécifié.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- Lecteur Windows Media de la méthode getByAuthor
- méthode getByAuthor Lecteur Windows Media, classe MediaCollection
- Lecteur Windows Media de la classe MediaCollection, méthode getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87989d38d49ff87ce26b7394f4ee79ef4bd7197cd0e35dcd5316797df401ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574626"
---
# <a name="mediacollectiongetbyauthor-method"></a>Méthode MediaCollection. getByAuthor

La méthode **getByAuthor** récupère une sélection des éléments multimédias par l’auteur spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*auteur* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’auteur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise *MediaCollection*. **getByAuthor** pour récupérer une sélection d’éléments multimédias. La sélection contient des éléments correspondant à l’auteur spécifié par l’utilisateur dans un élément d’entrée de texte HTML nommé GetAuthor. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
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

 

 





