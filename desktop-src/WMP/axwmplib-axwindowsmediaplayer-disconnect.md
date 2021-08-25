---
title: Événement Disconnect de l’objet AxWindowsMediaPlayer
description: L’événement Disconnect est réservé pour une utilisation ultérieure.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- événement disconnect de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0554de8fe71ae13e510733ed2204ff4ed79d575a40f23a1769a5fb36eeb560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902691"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a>Événement Disconnect de l’objet AxWindowsMediaPlayer

L’événement Disconnect est réservé pour une utilisation ultérieure.

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                               |
|----------|-------------------------------------------|
| result   | **System. Int32** Non pris en charge.<br/> |



 

## <a name="remarks"></a>Remarques

Cet événement est réservé à une utilisation ultérieure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





