---
title: Événement Warning de l’objet AxWindowsMediaPlayer
description: L’événement d’avertissement est réservé à une utilisation ultérieure.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- événement d’avertissement de l’objet AxWindowsMediaPlayer Lecteur Windows Media
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
ms.openlocfilehash: 18925236148a508e66bb34e83f7ddb69f0cb59d87c98dfe0188f780ea2fc3605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003999"
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

 

 





