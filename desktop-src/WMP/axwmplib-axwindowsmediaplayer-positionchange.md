---
title: Événement PositionChange de l’objet AxWindowsMediaPlayer
description: L’événement PositionChange se produit lorsque la position de lecture actuelle dans l’élément multimédia a été modifiée.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Événement PositionChange de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544079"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>Événement PositionChange de l’objet AxWindowsMediaPlayer

L’événement PositionChange se produit lorsque la position de lecture actuelle dans l’élément multimédia a été modifiée.

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété    | Description                                         |
|-------------|-----------------------------------------------------|
| oldPosition | System. DoubleSpecifies l’ancienne position.<br/> |
| newPosition | System. DoubleSpecifies la nouvelle position.<br/> |



 

## <a name="remarks"></a>Notes

Cet événement n’est pas déclenché régulièrement pendant la lecture. Il se produit uniquement quand une modification active la position actuelle de l’élément multimédia en cours de exécution, par exemple lorsque l’utilisateur déplace la poignée de recherche ou lorsque le code est exécuté et spécifie une valeur pour IWMPControls. **CurrentPosition**.

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

[**IWMPControls. currentPosition (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





