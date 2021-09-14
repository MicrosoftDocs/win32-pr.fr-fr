---
title: Méthode IWMPControls playItem
description: La méthode playItem lit l’élément multimédia spécifié. | Méthode IWMPControls playItem
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- Lecteur Windows Media de la méthode playItem
- méthode playItem Lecteur Windows Media, interface IWMPControls
- Lecteur Windows Media de l’interface IWMPControls, méthode playItem
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010752"
---
# <a name="iwmpcontrolsplayitem-method"></a>IWMPControls ::p méthode layItem

La méthode **playItem** lit l’élément multimédia spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIWMPMedia* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPMedia** pour l’élément multimédia.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L’élément multimédia est chargé et lu automatiquement, quelle que soit la valeur de la propriété **IWMPSettings. AutoStart** . Pour charger un élément sans le lire automatiquement, définissez **IWMPSettings. AutoStart** sur **false** et affectez une valeur à **AxWindowsMediaPlayer. URL**, après quoi **IWMPControls. Play** peut être appelé pour démarrer la lecture de l’élément.

Remarque

**playItem** fonctionne uniquement avec les éléments dans **AxWindowsMediaPlayer. currentPlaylist**. L’appel de **playItem** avec une référence à un élément multimédia enregistré n’est pas pris en charge.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **playItem** pour lire un élément multimédia à partir de la sélection actuelle. L’élément à lire est choisi en fonction de sa position dans la sélection. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB et C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. play (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. Item (VB et C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. autostart (VB et C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





