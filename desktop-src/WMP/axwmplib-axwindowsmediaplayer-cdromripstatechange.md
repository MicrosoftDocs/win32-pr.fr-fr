---
title: Événement CdromRipStateChange de l’objet AxWindowsMediaPlayer
description: L’événement CdromRipStateChange se produit lorsqu’une opération d’extraction de CD change d’État.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- événement CdromRipStateChange de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416266"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a>Événement CdromRipStateChange de l’objet AxWindowsMediaPlayer

L’événement CdromRipStateChange se produit lorsqu’une opération d’extraction de CD change d’État.

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété  | Description                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| pCdromRip | Interface WMPLib. IWMPCdromRipThe qui représente l’opération d’extraction qui a déclenché l’erreur.<br/> |
| wmprs     | Valeur d’énumération WMPLib. WMPRipStateThe qui indique le nouvel État.<br/>                         |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11<br/>                                                                                         |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdromRip (VB et C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





