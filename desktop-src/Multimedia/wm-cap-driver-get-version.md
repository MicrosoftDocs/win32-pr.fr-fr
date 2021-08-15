---
title: Message WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: Le \_ message WM Cap \_ Driver \_ obtenir \_ la version retourne les informations de version du pilote de capture connecté à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- message WM_CAP_DRIVER_GET_VERSION Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6bed4513383c5dd889639a78e9f00e409fe347bfd6b64b112ea830571ae55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687089"
---
# <a name="wm_cap_driver_get_version-message"></a>Message de la version du \_ pilote WM Cap \_ \_ \_

Le message **WM \_ Cap \_ Driver obtenir la \_ \_ version** retourne les informations de version du pilote de capture connecté à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la mémoire tampon définie par l’application référencée par **szVer**.

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*
</dt> <dd>

Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner les informations de version sous la forme d’une chaîne terminée par le caractère null.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.

## <a name="remarks"></a>Remarques

Les informations de version sont une chaîne de texte Récupérée à partir de la zone de ressources du pilote. Les applications doivent allouer environ 40 octets pour cette chaîne. Si les informations de version ne sont pas disponibles, une chaîne **null** est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 

 





