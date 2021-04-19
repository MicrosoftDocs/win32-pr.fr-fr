---
title: Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer
description: L’événement AudioLanguageChange se produit lorsque le langage audio actuel change. | Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525107"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>Événement AudioLanguageChange de l’objet AxWindowsMediaPlayer

L’événement AudioLanguageChange se produit lorsque le langage audio actuel change.

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété   | Description                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **langID** | **System. Int32** Identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.<br/> |



 

## <a name="remarks"></a>Notes

Un identificateur de paramètres régionaux (LCID) identifie de manière unique un dialecte de langage particulier, appelé paramètres régionaux.

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

[**IWMPControls3. currentAudioLanguage (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





