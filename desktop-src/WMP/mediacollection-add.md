---
title: MediaCollection. Add, méthode
description: La méthode Add ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque. | MediaCollection. Add, méthode
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Ajouter une méthode lecteur Windows Media
- Add, méthode lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode Add
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525541"
---
# <a name="mediacollectionadd-method"></a>MediaCollection. Add, méthode

La méthode **Add** ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*chemin d’accès* \[ dans\]
</dt> <dd>

**Chaîne** contenant le chemin d’accès.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **multimédia** .

## <a name="remarks"></a>Notes

Cette méthode charge un élément multimédia existant ou une sélection dans la bibliothèque, en fonction d’un chemin d’accès à un fichier. Cette méthode ne déplace pas ou ne modifie pas le fichier. Cette méthode échoue si le chemin d’accès local n’est pas valide, mais que la validité des fichiers multimédias numériques n’est pas vérifiée avant leur ajout à la bibliothèque.

Cette méthode accepte à la fois les fichiers de sélection statique et automatique. *PlaylistCollection*. la méthode **importPlaylist** peut également être utilisée pour ajouter une sélection statique à la bibliothèque.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple Microsoft JScript suivant ajoute trois objets multimédias à la collection de supports du lecteur Windows Media. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection. Remove**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





