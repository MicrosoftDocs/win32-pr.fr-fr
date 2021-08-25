---
title: Événement CdromBurnError de l’objet AxWindowsMediaPlayer
description: L’événement CdromBurnError se produit lorsqu’une erreur générique se produit pendant une opération de gravure de CD.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- événement CdromBurnError de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ea2ca4c510685e8a9d23a3fdc507e055f30c8916c7bf8bbbfbb30a5c4591b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864739"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>Événement CdromBurnError de l’objet AxWindowsMediaPlayer

L’événement CdromBurnError se produit lorsqu’une erreur générique se produit pendant une opération de gravure de CD.

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété   | Description                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| hrError    | **System. Int32** Erreur qui a déclenché l’événement.<br/>                                               |
| pCdromBurn | Interface WMPLib. IWMPCdromBurnThe qui représente l’opération de gravure qui a déclenché l’erreur.<br/> |



 

## <a name="remarks"></a>Remarques

Pour capturer les erreurs spécifiques au support, gérez le AxWMPLib. \_ \_Événement WMPOCXEvents CdromBurnMediaError.

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

[**événement AxWindowsMediaPlayer. CdromBurnMediaError (VB et C#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





