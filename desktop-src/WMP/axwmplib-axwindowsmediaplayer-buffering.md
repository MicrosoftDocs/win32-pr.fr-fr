---
title: Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer
description: L’événement de mise en mémoire tampon se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement. | Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530940"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer

L’événement de mise en mémoire tampon se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement.

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété | Description                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Démarrer    | System. BooleanSpecifies indique si la mise en mémoire tampon a commencé ou s’est terminée. La valeur true indique qu’elle a commencé ; la valeur false indique qu’elle est terminée.<br/> |



 

## <a name="remarks"></a>Notes

Utilisez cet événement pour déterminer quand la mise en mémoire tampon ou le téléchargement démarre ou s’arrête. Vous pouvez utiliser le même bloc d’événements pour les cas et les *IWMPNetwork* de test. **bufferingProgress** et *IWMPNetwork*. **downloadProgress** pour déterminer si le lecteur Windows Media met actuellement en mémoire tampon ou télécharge le contenu.

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

[**IWMPNetwork. bufferingProgress (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. downloadProgress (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





