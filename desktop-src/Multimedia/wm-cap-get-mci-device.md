---
title: Message WM_CAP_GET_MCI_DEVICE (VFW. h)
description: Le \_ message WM \_ Cap \_ obtenir \_ un appareil MCI récupère le nom d’un périphérique MCI précédemment défini avec le \_ message WM Cap \_ Set \_ MCI \_ Device. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- message WM_CAP_GET_MCI_DEVICE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9471177693bfbd5646d93e8487395cdf330b8281a1f43fa00d79dc690e6d718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800651"
---
# <a name="wm_cap_get_mci_device-message"></a>Message de l’appareil WM d’accès à \_ \_ \_ MCI \_

Le message **WM \_ Cap obtenir un \_ \_ \_ appareil MCI** récupère le nom d’un périphérique MCI précédemment défini avec le message [**WM \_ Cap \_ Set \_ MCI \_ Device**](wm-cap-set-mci-device.md) . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Longueur, en octets, de la mémoire tampon référencée par **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du périphérique MCI.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

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

 

 





