---
title: Événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale. | Événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee9555b3efc4cb95b164fc8922b1ce4253613fbd2c45c0624a3d61d0fa7a9f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135982"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a>Événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer

L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale.

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | Élément multimédia System. ObjectThe supprimé de la bibliothèque locale. Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.<br/> |



 

## <a name="remarks"></a>Remarques

Cet événement se produit uniquement pour la bibliothèque locale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11<br/>                                                                                         |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





