---
title: Événement PlaylistChange de l’objet AxWindowsMediaPlayer
description: L’événement PlaylistChange se produit lorsqu’une sélection est modifiée. | Événement PlaylistChange de l’objet AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Événement PlaylistChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543916"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>Événement PlaylistChange de l’objet AxWindowsMediaPlayer

L’événement PlaylistChange se produit lorsqu’une sélection est modifiée.

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété     | Description                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| **playlist** | Objet System. ObjectThe qui a été modifié. Vous pouvez effectuer un cast de ce en une interface IWMPPlaylist pour y accéder.<br/>                |
| **change**   | Valeur d’énumération WMPLib. WMPPlaylistChangeEventTypeAn indiquant le type de modification qui s’est produite dans la sélection.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





