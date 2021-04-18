---
title: Événement Warning de l’objet AxWindowsMediaPlayer
description: L’événement d’avertissement est réservé à une utilisation ultérieure.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Événement d’avertissement de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526802"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>Événement Warning de l’objet AxWindowsMediaPlayer

L’événement d’avertissement est réservé à une utilisation ultérieure.

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ WarningEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété    | Description                                |
|-------------|--------------------------------------------|
| warningType | **System. Int32** Non pris en charge.<br/>  |
| param       | **System. Int32** Non pris en charge.<br/>  |
| description | **System. String** Non pris en charge.<br/> |



 

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

 

 





