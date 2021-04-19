---
title: Événement CdromBurnStateChange de l’objet AxWindowsMediaPlayer
description: L’événement CdromBurnStateChange se produit lorsqu’une opération de gravure de CD change d’État.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Événement CdromBurnStateChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528590"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>Événement CdromBurnStateChange de l’objet AxWindowsMediaPlayer

L’événement CdromBurnStateChange se produit lorsqu’une opération de gravure de CD change d’État.

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété   | Description                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pCdromBurn | Interface WMPLib. IWMPCdromBurnThe qui représente l’opération de gravure qui a déclenché l’erreur.<br/> |
| wmpbs      | Valeur d’énumération WMPLib. WMPBurnStateThe qui indique le nouvel État.<br/>                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11<br/>                                                                                         |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





