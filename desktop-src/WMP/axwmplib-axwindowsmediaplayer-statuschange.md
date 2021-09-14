---
title: Événement StatusChange de l’objet AxWindowsMediaPlayer
description: L’événement StatusChange se produit lorsque la propriété Status change de valeur. | Événement StatusChange de l’objet AxWindowsMediaPlayer
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- événement StatusChange de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193327"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a>Événement StatusChange de l’objet AxWindowsMediaPlayer

L’événement **statuschange** se produit lorsque la propriété **Status** change de valeur.

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a>Données d'événements

Cet événement ne contient pas de données.

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

[**AxWindowsMediaPlayer. status (VB et C#)**](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





