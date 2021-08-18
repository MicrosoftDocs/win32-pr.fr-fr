---
title: Événement KeyUp de l’objet AxWindowsMediaPlayer
description: L’événement KeyUp se produit lorsqu’une touche est relâchée. | Événement KeyUp de l’objet AxWindowsMediaPlayer
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- événement KeyUp de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a2666268e2c12e74c6498446ff49bde69dd30cf9819a7899e88a8b8ee4466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136012"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a>Événement KeyUp de l’objet AxWindowsMediaPlayer

L’événement KeyUp se produit lorsqu’une touche est relâchée.

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété    | Description                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies quelle touche physique est enfoncée. Pour connaître les valeurs possibles, consultez la section Notes de l’événement KeyOut.<br/>                                                                                                                                                                                                                                                   |
| nShiftState | Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. L’argument Shift indique l’état de ces clés. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.<br/> |



 

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

 

 





