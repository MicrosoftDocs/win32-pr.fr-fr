---
title: Événement ModeChange de l’objet AxWindowsMediaPlayer
description: L’événement ModeChange se produit lorsqu’un mode du lecteur Windows Media est modifié. | Événement ModeChange de l’objet AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Événement ModeChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534777"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>Événement ModeChange de l’objet AxWindowsMediaPlayer

L’événement ModeChange se produit lorsqu’un mode du lecteur Windows Media est modifié.

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété | Description                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| modeName | System. StringIndicates le mode qui a été modifié. Pour connaître les valeurs possibles, consultez la section Notes.<br/> |
| newValue | System. BooleanIndicates : nouvel État du mode spécifié.<br/>                        |



 

## <a name="remarks"></a>Notes

Le tableau suivant indique les valeurs possibles pour la propriété modeName.



| String  | Description                                         |
|---------|-----------------------------------------------------|
| lecture aléatoire | Les pistes sont lues dans un ordre aléatoire.                  |
| loop    | L’intégralité de la séquence de pistes est lue à plusieurs reprises. |



 

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

[**IWMPSettings. getMode (VB et C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB et C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





