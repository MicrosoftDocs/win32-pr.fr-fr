---
title: Événement CdromBurnMediaError de l’objet AxWindowsMediaPlayer
description: L’événement CdromBurnMediaError se produit lorsqu’une erreur se produit lors de la gravure d’un élément multimédia individuel sur un CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- événement CdromBurnMediaError de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba161945edcda7409b842987ab97768c30a6e1f0ba011772cf7f3757d3f61c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765268"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Événement CdromBurnMediaError de l’objet AxWindowsMediaPlayer

L’événement CdromBurnMediaError se produit lorsqu’une erreur se produit lors de la gravure d’un élément multimédia individuel sur un CD.

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété   | Description                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromBurn | Interface WMPLib. IWMPCdromBurnThe qui représente l’opération de gravure qui a déclenché l’erreur.<br/>               |
| pMedia     | Élément multimédia System. ObjectThe qui a généré l’erreur. Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.<br/> |



 

## <a name="remarks"></a>Remarques

Pour capturer des erreurs génériques, gérez AxWMPLib. \_ \_Événement WMPOCXEvents CdromBurnError.

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

[**événement AxWindowsMediaPlayer. CdromBurnError (VB et C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





