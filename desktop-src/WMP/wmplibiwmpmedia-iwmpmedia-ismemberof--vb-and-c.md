---
title: Méthode IWMPMedia isMemberOf
description: La méthode isMemberOf retourne une valeur indiquant si l’élément multimédia spécifié est membre de la sélection spécifiée.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- Lecteur Windows Media de la méthode isMemberOf
- méthode isMemberOf Lecteur Windows Media, interface IWMPMedia
- Lecteur Windows Media de l’interface IWMPMedia, méthode isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416152"
---
# <a name="iwmpmediaismemberof-method"></a>IWMPMedia :: isMemberOf, méthode

La méthode **isMemberOf** retourne une valeur indiquant si l’élément multimédia spécifié est membre de la sélection spécifiée.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPlaylist* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPPlaylist** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Valeur **System. Boolean** qui indique si l’élément multimédia est membre de la sélection.

## <a name="remarks"></a>Notes

Cette méthode ne peut pas vérifier les sélections récupérées par le biais de l’interface **IWMPMediaCollection** . Pour déterminer si un élément multimédia est membre d’une sélection nommée particulière, récupérez la collection de sélections avec la propriété **AxWindowsMediaPlayer. playlistCollection** . Une fois que vous récupérez la collection, récupérez la playlist en appelant la méthode **IWMPPlaylistCollection. GetByName** .

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple suivant utilise **isMemberOf** pour déterminer si l’élément multimédia actuel est membre de la sélection nommée All Musique. Si ce n’est pas le cas, l’élément multimédia actuel est ajouté à la sélection. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. playlistCollection (VB et C#)**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





