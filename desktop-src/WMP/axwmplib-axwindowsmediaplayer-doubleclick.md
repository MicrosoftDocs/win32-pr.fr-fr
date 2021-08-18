---
title: Événement DoubleClick de l’objet AxWindowsMediaPlayer
description: l’événement DoubleClick se produit lorsque l’utilisateur double-clique sur un bouton de la souris sur un contrôle de Lecteur Windows Media.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- événement DoubleClick de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb01a5d0d5b9dd750c1232badb913000218a088d1ba6b41bc22e4e5dd49a6230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136102"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a>Événement DoubleClick de l’objet AxWindowsMediaPlayer

l’événement DoubleClick se produit lorsque l’utilisateur double-clique sur un bouton de la souris sur un contrôle de Lecteur Windows Media.

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété    | Description                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nbouton     | Champ de bits System. Int16a avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.<br/>                                                |
| nShiftState | Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.<br/> |
| Rotation          | Coordonnée x de System. Int32The du pointeur de la souris par rapport au coin supérieur gauche du contrôle.<br/>                                                                                                                                                                                                                 |
| Années          | Coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.<br/>                                                                                                                                                                                                                 |



 

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

 

 





