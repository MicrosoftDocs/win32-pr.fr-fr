---
title: IWMPMedia propriété sourceURL
description: La propriété sourceURL obtient l’URL de l’élément multimédia.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- Lecteur Windows Media de la propriété sourceURL
- Lecteur Windows Media de la propriété sourceURL, interface IWMPMedia
- Lecteur Windows Media de l’interface IWMPMedia, propriété sourceURL
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122677"
---
# <a name="iwmpmediasourceurl-property"></a>IWMPMedia :: sourceURL, propriété

La propriété **sourceURL** obtient l’URL de l’élément multimédia.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est l’URL source.

## <a name="examples"></a>Exemples

l’exemple suivant utilise **sourceURL** pour récupérer l’URL du premier élément multimédia dans la sélection « All Musique ». l’URL de l’élément multimédia est ensuite affectée à la propriété URL de l’objet lecteur. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





