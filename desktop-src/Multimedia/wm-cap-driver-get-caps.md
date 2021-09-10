---
title: Message WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: Le \_ message WM Cap \_ Driver to Cap \_ \_ retourne les fonctionnalités matérielles du pilote de capture actuellement connecté à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- message WM_CAP_DRIVER_GET_CAPS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367884"
---
# <a name="wm_cap_driver_get_caps-message"></a>Message d’accès aux \_ \_ \_ majuscules du pilote WM Cap \_

Le message **WM \_ Cap Driver to Cap \_ \_ \_** retourne les fonctionnalités matérielles du pilote de capture actuellement connecté à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la structure référencée par **s**.

</dd> <dt>

<span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*
</dt> <dd>

Pointeur vers la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) pour contenir les fonctionnalités matérielles.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.

## <a name="remarks"></a>Remarques

Les fonctionnalités retournées dans [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) sont constantes pour un pilote de capture donné. Les applications doivent récupérer ces informations une seule fois lorsque le pilote de capture est connecté pour la première fois à une fenêtre de capture.

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

 

 





