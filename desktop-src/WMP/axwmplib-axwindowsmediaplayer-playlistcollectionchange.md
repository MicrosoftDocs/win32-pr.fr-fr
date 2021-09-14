---
title: Événement PlaylistCollectionChange de l’objet AxWindowsMediaPlayer
description: L’événement PlaylistCollectionChange se produit lorsqu’une modification est apportée à la collection de sélections. | Événement PlaylistCollectionChange de l’objet AxWindowsMediaPlayer
ms.assetid: 868ee1c6-b740-4614-90ac-961c59091f0f
keywords:
- événement PlaylistCollectionChange de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7dd88b558bb13b8835be1a8f840df8f8316706
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855916"
---
# <a name="playlistcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>Événement PlaylistCollectionChange de l’objet AxWindowsMediaPlayer

L’événement PlaylistCollectionChange se produit lorsqu’une modification est apportée à la collection de sélections.

``` syntax
[C#]
private void player_PlaylistCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_PlaylistCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.PlaylistCollectionChange
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
</dt> </dl>

 

 





