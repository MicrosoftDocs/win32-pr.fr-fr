---
title: Événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer
description: L’événement PlaylistCollectionPlaylistAdded se produit lorsqu’une sélection est ajoutée à la collection de sélections. | Événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855910"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>Événement PlaylistCollectionPlaylistAdded de l’objet AxWindowsMediaPlayer

L’événement PlaylistCollectionPlaylistAdded se produit lorsqu’une sélection est ajoutée à la collection de sélections.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété             | Description                                                                |
|----------------------|----------------------------------------------------------------------------|
| **bstrPlaylistName** | System. StringSpecifies nom de la sélection qui a été ajoutée.<br/> |



 

## <a name="remarks"></a>Notes

Le nom de la sélection ajoutée peut être utilisé pour récupérer la playlist correspondante à l’aide de IWMPPlaylistCollection. méthode **GetByName** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





