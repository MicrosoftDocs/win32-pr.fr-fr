---
title: Événement CdromMediaChange de l’objet AxWindowsMediaPlayer
description: L’événement CdromMediaChange se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD. | Événement CdromMediaChange de l’objet AxWindowsMediaPlayer
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- événement CdromMediaChange de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416268"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a>Événement CdromMediaChange de l’objet AxWindowsMediaPlayer

L’événement **CdromMediaChange** se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD.

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                                                        |
|----------|--------------------------------------------------------------------|
| CdromNum | System. Int32Specifies l’index du lecteur de CD ou de DVD.<br/> |



 

## <a name="remarks"></a>Notes

L’index du lecteur de CD correspond à l’index d’une interface IWMPCdrom accessible via l’interface IWMPCdromCollection.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdrom (VB et C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdromCollection (VB et C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





