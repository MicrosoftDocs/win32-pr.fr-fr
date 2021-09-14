---
title: Événement Click de l’objet AxWindowsMediaPlayer
description: l’événement Click se produit lorsque l’utilisateur clique sur un bouton de la souris sur un contrôle Lecteur Windows Media.
ms.assetid: 41a719a2-103a-46b5-806d-5c21c4a09e00
keywords:
- événement Click de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- Click Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d316e5dc4c12e75d75dd0b292c1df6db974bc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856029"
---
# <a name="click-event-of-the-axwindowsmediaplayer-object"></a>Événement Click de l’objet AxWindowsMediaPlayer

l’événement Click se produit lorsque l’utilisateur clique sur un bouton de la souris sur un contrôle Lecteur Windows Media.

``` syntax
[C#]
private void player_OnClick(
  object  sender,
  _WMPOCXEvents_ClickEvent e
);

[Visual Basic]
Private Sub player_OnClick(  
  sender As Object,
  e As WMPOCXEvents_ClickEvent
) Handles player.ClickEvent
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ ClickEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ ClickEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété    | Description                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nbouton     | Champ de bits System. Int16a avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.<br/>                                                |
| nShiftState | Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.<br/> |
| Rotation          | Coordonnée x de System. Int32The du pointeur de la souris par rapport au coin supérieur gauche du contrôle.<br/>                                                                                                                                                                                                                 |
| Années          | Coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.<br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





