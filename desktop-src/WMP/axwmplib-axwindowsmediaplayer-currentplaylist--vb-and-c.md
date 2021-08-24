---
title: AxWindowsMediaPlayer. currentPlaylist, propriété
description: La propriété currentPlaylist obtient ou définit l’interface IWMPPlaylist actuelle qui fournit un moyen simple d’organiser et de manipuler des éléments multimédias dans une liste.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Lecteur Windows Media de la propriété currentPlaylist
- Lecteur Windows Media de la propriété currentPlaylist, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f976084773a333e40c0a278878e9a35ed913e5911ec732c0dccfe6525e5f45a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765260"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>AxWindowsMediaPlayer. currentPlaylist, propriété

La propriété currentPlaylist obtient ou définit l’interface **IWMPPlaylist** actuelle qui fournit un moyen simple d’organiser et de manipuler des éléments multimédias dans une liste.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valeur de la propriété

Interface WMPLib. IWMPPlaylist qui fournit l’accès à la sélection actuelle.

## <a name="remarks"></a>Remarques

Si la propriété IWMPSettings. AutoStart (également accessible via AxWindowsMediaPlayer. Settings.**AutoStart**) a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentPlaylist**.

Cette propriété prend une interface IWMPPlaylist, qui peut être acquise de plusieurs façons, par exemple en obtenant la valeur de *IWMPPlaylistArray*. **Item** ou *IWMPPlaylistCollection*. Propriétés de **newPlaylist** . Pour charger un élément de **sélection** à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez AxWindowsMediaPlayer. **newPlaylist**.

## <a name="examples"></a>Exemples

L’exemple suivant récupère la première sélection de la bibliothèque et utilise la propriété currentPlaylist pour définir la sélection Récupérée comme playlist actuelle et afficher son nom. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. newPlaylist (VB et C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer. settings (VB et C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Item (VB et C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. newPlaylist (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. autostart (VB et C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





