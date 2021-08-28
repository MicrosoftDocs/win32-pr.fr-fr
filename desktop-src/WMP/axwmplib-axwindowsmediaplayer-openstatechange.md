---
title: Événement OpenStateChange de l’objet AxWindowsMediaPlayer
description: L’événement OpenStateChange se produit lorsque la propriété openState change de valeur. | Événement OpenStateChange de l’objet AxWindowsMediaPlayer
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- événement OpenStateChange de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ccf7619e86268fe6b465d2a64ca00d650a7a7051b3aa4f44e2a73a98929be13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003979"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a>Événement OpenStateChange de l’objet AxWindowsMediaPlayer

L’événement OpenStateChange se produit lorsque la propriété **openState** change de valeur.

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NewState | System. Int32Specifies : nouvel état ouvert. Pour obtenir une table de valeurs, consultez [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).<br/> |



 

## <a name="remarks"></a>Remarques

Lecteur Windows Media pouvez parcourir plusieurs états ouverts pendant qu’il tente d’ouvrir un fichier réseau, par exemple en localisant le serveur, en se connectant au serveur et enfin en ouvrant le fichier. Cet événement est déclenché chaque fois que l’état ouvert change.

il n’est pas garanti que les états de Lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

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

[**AxWindowsMediaPlayer. openState (VB et C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





