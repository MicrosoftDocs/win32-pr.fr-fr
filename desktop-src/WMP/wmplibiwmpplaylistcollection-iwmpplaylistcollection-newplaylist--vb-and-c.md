---
title: Méthode IWMPPlaylistCollection newPlaylist
description: La méthode newPlaylist retourne une interface IWMPPlaylist pour une nouvelle playlist vide dans la bibliothèque.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- Lecteur Windows Media de la méthode newPlaylist
- méthode newPlaylist Lecteur Windows Media, interface IWMPPlaylistCollection
- Lecteur Windows Media de l’interface IWMPPlaylistCollection, méthode newPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411281"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>IWMPPlaylistCollection :: newPlaylist, méthode

La méthode **newPlaylist** retourne une interface **IWMPPlaylist** pour une nouvelle playlist vide dans la bibliothèque.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrName* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de la nouvelle sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Interface **wmplib. IWMPPlaylist** pour la nouvelle sélection.

## <a name="remarks"></a>Notes

Cette méthode crée une sélection vide dans la bibliothèque. Pour remplir la sélection avec des éléments multimédias, utilisez **IWMPPlaylist. appendItem** ou **IWMPPlaylist. InsertItem**.

Plusieurs playlists portant le même nom sont autorisées dans la bibliothèque. Pour éviter de créer un nom de playlist dupliqué avec cette méthode, utilisez la méthode **GetByName** et **IWMPPlaylistArray. Count** pour déterminer si une sélection portant un nom particulier existe déjà.

Les espaces de début et de fin ne sont pas autorisés dans les noms de playlist et sont automatiquement supprimés de la valeur spécifiée pour le paramètre *bstrName* .

Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant crée une nouvelle sélection vide appelée « ThreeList », l’ajoute à la collection de sélections et lui retourne une interface. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. count (VB et C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB et C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





