---
title: Événement EndOfStream de l’objet AxWindowsMediaPlayer
description: L’événement EndOfStream est réservé pour une utilisation ultérieure.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Événement EndOfStream de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540152"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a>Événement EndOfStream de l’objet AxWindowsMediaPlayer

L’événement EndOfStream est réservé pour une utilisation ultérieure.

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                           |
|----------|---------------------------------------|
| result   | System. Int32Not pris en charge.<br/> |



 

## <a name="remarks"></a>Notes

Cet événement est réservé à une utilisation ultérieure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





