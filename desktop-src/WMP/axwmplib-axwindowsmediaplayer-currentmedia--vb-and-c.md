---
title: AxWindowsMediaPlayer. currentMedia, propriété
description: La propriété currentMedia obtient ou définit l’interface IWMPMedia qui correspond à l’élément multimédia actuel.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- Lecteur Windows Media de la propriété currentMedia
- Lecteur Windows Media de la propriété currentMedia, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027949872b2ff988fcfcad5a8464d9a48ed69d3389ddbca0ad4f91b2d9e3c8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098839"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>AxWindowsMediaPlayer. currentMedia, propriété

La propriété currentMedia obtient ou définit l’interface IWMPMedia qui correspond à l’élément multimédia actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>Valeur de la propriété

Interface WMPLib. IWMPMedia qui fournit l’accès à l’élément multimédia actuel.

## <a name="remarks"></a>Remarques

Si AxWindowsMediaPlayer. Settings. la propriété **AutoStart** a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentMedia**.

Vous pouvez récupérer une interface IWMPMedia pour un élément multimédia donné via la propriété IWMPPlaylist. Item (méthode IWMPPlaylist. obtenir un \_ élément en C#). Pour charger un élément multimédia à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez newMedia.

## <a name="examples"></a>Exemples

L’exemple suivant récupère le premier élément multimédia de la bibliothèque et utilise la propriété currentMedia pour définir l’élément multimédia récupéré comme élément multimédia actuel et afficher son nom. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
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

[**AxWindowsMediaPlayer. newMedia (VB et C#)**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. Item (VB et C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. autostart (VB et C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





