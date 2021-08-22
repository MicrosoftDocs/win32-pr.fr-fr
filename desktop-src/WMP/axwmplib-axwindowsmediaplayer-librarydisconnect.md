---
title: Événement LibraryDisconnect de l’objet AxWindowsMediaPlayer
description: L’événement LibraryDisconnect se produit lorsqu’une bibliothèque n’est plus disponible.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- événement LibraryDisconnect de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a032dc95a68430768b0f2aa109a56dae80cdaecb14b67eb5dbf6b2657cdd5107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136002"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>Événement LibraryDisconnect de l’objet AxWindowsMediaPlayer

L’événement LibraryDisconnect se produit lorsqu’une bibliothèque n’est plus disponible.

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| pLibrary | **Wmplib. IWMPLibrary** Interface qui représente la bibliothèque déconnectée.<br/> |



 

## <a name="remarks"></a>Remarques

Cet événement ne se produit pas pour la bibliothèque locale.

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

[**Interface IWMPLibrary (VB et C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





