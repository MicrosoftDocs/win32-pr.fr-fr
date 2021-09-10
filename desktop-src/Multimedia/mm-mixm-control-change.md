---
title: Message MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: Le \_ \_ message de modification du contrôle MIXM mm \_ est envoyé par un appareil de mixage pour avertir une application que l’état d’un contrôle associé à une ligne audio a changé. L’application doit actualiser son affichage et les valeurs mises en cache pour le contrôle spécifié.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- message MM_MIXM_CONTROL_CHANGE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367564"
---
# <a name="mm_mixm_control_change-message"></a>\_Message de \_ modification du contrôle MIXM mm \_

Le message de **\_ \_ \_ modification du contrôle MIXM mm** est envoyé par un appareil de mixage pour avertir une application que l’état d’un contrôle associé à une ligne audio a changé. L’application doit actualiser son affichage et les valeurs mises en cache pour le contrôle spécifié.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Handle vers le périphérique de mixage (**HMIXER**) qui a envoyé le message de notification.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*
</dt> <dd>

Identificateur de contrôle pour le contrôle de mixage qui a changé d’État. Cet identificateur est le même que le membre **dwControlID** de la structure **MIXERCONTROL** retournée par la fonction **mixerGetLineControls**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une application doit ouvrir un dispositif de mixage et spécifier une fenêtre de rappel pour recevoir le message de **\_ modification de \_ contrôle \_ mm MIXM** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Mixages audio](audio-mixers.md)
</dt> <dt>

[Messages de Mixer Audio](audio-mixer-messages.md)
</dt> </dl>

 

 





