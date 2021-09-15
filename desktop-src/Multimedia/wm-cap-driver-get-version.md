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
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413850"
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

## <a name="remarks"></a>Notes

Les informations de version sont une chaîne de texte Récupérée à partir de la zone de ressources du pilote. Les applications doivent allouer environ 40 octets pour cette chaîne. Si les informations de version ne sont pas disponibles, une chaîne **null** est retournée.

## <a name="requirements"></a>Spécifications



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

 

 





