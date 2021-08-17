---
title: Événement CdromRipMediaError de l’objet AxWindowsMediaPlayer
description: L’événement CdromRipMediaError se produit lorsqu’une erreur se produit lors de l’extraction d’une piste individuelle à partir d’un CD.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- événement CdromRipMediaError de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2be1f777c4af3385e41939743bb91a20d3d7094f1a38917b3e79686b2a2863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136182"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Événement CdromRipMediaError de l’objet AxWindowsMediaPlayer

L’événement CdromRipMediaError se produit lorsqu’une erreur se produit lors de l’extraction d’une piste individuelle à partir d’un CD.

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété  | Description                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromRip | Interface WMPLib. IWMPCdromRipThe qui représente l’opération d’extraction qui a déclenché l’erreur.<br/>                |
| pMedia    | Élément multimédia System. ObjectThe qui a généré l’erreur. Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.<br/> |



 

## <a name="requirements"></a>Configuration requise



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

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





