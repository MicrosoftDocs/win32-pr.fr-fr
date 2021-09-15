---
title: Propriété de la sélection IWMPCdrom
description: La propriété playlist obtient une interface IWMPPlaylist représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour un DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Lecteur Windows Media de propriétés de la sélection
- Lecteur Windows Media de propriété Playlist, interface IWMPCdrom
- Lecteur Windows Media de l’interface IWMPCdrom, propriété Playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530225"
---
# <a name="iwmpcdromplaylist-property"></a>IWMPCdrom ::P propriété laylist

La propriété **playlist** obtient une interface **IWMPPlaylist** représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour un DVD.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Valeur de la propriété

Interface **wmplib. IWMPPlaylist** .

## <a name="remarks"></a>Notes

En général, le contenu basé sur DVD est organisé en titres. Chaque titre contient un ou plusieurs chapitres. Chaque DVD étant créé différemment, la façon dont les titres et les chapitres sont utilisés est celle de l’auteur du contenu.

Pour un DVD, cette propriété obtient une sélection qui contient comme premier élément une interface **IWMPMedia** nommée « DVD ». Cette interface représente le support DVD. La lecture de l’élément entraîne la lecture du DVD à partir du début s’il s’agit de la première lecture après l’insertion d’un nouveau DVD, ou la reprise de la lecture si le DVD est le même que le dernier DVD affiché. La définition de cet élément en tant qu’élément actuel pendant la lecture entraîne la lecture du DVD à partir du début.

Les éléments supplémentaires (représentés par les interfaces **IWMPMedia** ) de la sélection sont des titres de DVD représentés par des sélections imbriquées. lorsque vous affectez à **IWMPControls. currentItem** la valeur égal à l’un de ces éléments de sélection imbriqués, Lecteur Windows Media définit automatiquement la sélection imbriquée comme playlist actuelle après le début de la lecture du chapitre. Vous pouvez ensuite utiliser les propriétés de l’interface **IWMPPlaylist** , les méthodes et les événements associés pour travailler avec des chapitres DVD, qui sont également des éléments de sélection.

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise la **sélection** pour remplir une zone de texte multiligne, nommée myText, avec la liste de pistes du CD audio actuellement insérée dans le premier lecteur de CD. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdrom (VB et C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





