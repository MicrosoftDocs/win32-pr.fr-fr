---
title: Événement LibraryConnect de l’objet AxWindowsMediaPlayer
description: L’événement LibraryConnect se produit lorsqu’une bibliothèque devient disponible.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Événement LibraryConnect de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526417"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a>Événement LibraryConnect de l’objet AxWindowsMediaPlayer

L’événement LibraryConnect se produit lorsqu’une bibliothèque devient disponible.

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| pLibrary | **Wmplib. IWMPLibrary** Interface qui représente la bibliothèque connectée.<br/> |



 

## <a name="remarks"></a>Notes

Cet événement ne se produit pas pour la bibliothèque locale.

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

[**Interface IWMPLibrary (VB et C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





