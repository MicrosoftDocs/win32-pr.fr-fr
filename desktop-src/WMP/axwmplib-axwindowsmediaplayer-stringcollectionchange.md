---
title: Événement StringCollectionChange de l’objet AxWindowsMediaPlayer
description: L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change. | Événement StringCollectionChange de l’objet AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- événement StringCollectionChange de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ceeba7942be4180d02a44ff19d63c10f9bc9df0bba745fdf69bcf10e97c3052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764658"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>Événement StringCollectionChange de l’objet AxWindowsMediaPlayer

L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change.

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété              | Description                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| pdispStringCollection | Élément de collection de chaînes System. ObjectThe modifié. Vous pouvez effectuer un cast de ce en une interface IWMPStringCollection pour y accéder.<br/> |
| lCollectionIndex      | Index System. Int32The de l’élément de collection de chaînes qui a changé.<br/>                                                          |
| Modifier                | Valeur d’énumération WMPLib. WMPStringCollectionChangeEventTypeAn indiquant le type de modification qui s’est produite.<br/>                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB et C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**WMPStringCollectionChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





