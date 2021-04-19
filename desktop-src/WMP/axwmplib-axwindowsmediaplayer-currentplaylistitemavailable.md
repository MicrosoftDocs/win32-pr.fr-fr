---
title: Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer
description: L’événement CurrentPlaylistItemAvailable se produit lorsque la sélection actuelle est disponible. | Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539493"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer

L’événement CurrentPlaylistItemAvailable se produit lorsque la sélection actuelle est disponible.

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété         | Description                                                    |
|------------------|----------------------------------------------------------------|
| **bstrItemName** | Nom System. StringThe de l’élément de sélection en cours.<br/> |



 

## <a name="remarks"></a>Notes

Le nom de la sélection actuelle peut être utilisé pour récupérer l’interface **IWMPPlaylist** correspondante à partir de l’interface IWMPPlaylistArray qui est retournée à partir de la méthode IWMPPlaylistCollection. GetByName.

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
</dt> <dt>

[**Interface IWMPPlaylistArray (VB et C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





