---
title: Événement OpenStateChange de l’objet AxWindowsMediaPlayer
description: L’événement OpenStateChange se produit lorsque la propriété openState change de valeur. | Événement OpenStateChange de l’objet AxWindowsMediaPlayer
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Événement OpenStateChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
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
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538075"
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



 

## <a name="remarks"></a>Notes

Le lecteur Windows Media peut passer par plusieurs États ouverts pendant qu’il tente d’ouvrir un fichier réseau, par exemple Rechercher le serveur, se connecter au serveur et enfin ouvrir le fichier. Cet événement est déclenché chaque fois que l’état ouvert change.

Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. openState (VB et C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





