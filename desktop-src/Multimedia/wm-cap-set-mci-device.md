---
title: Message WM_CAP_SET_MCI_DEVICE (VFW. h)
description: Le \_ message WM Cap \_ Set \_ MCI \_ Device spécifie le nom du périphérique vidéo MCI à utiliser pour capturer les données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- Message WM_CAP_SET_MCI_DEVICE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740053"
---
# <a name="wm_cap_set_mci_device-message"></a>Message de l' \_ appareil WM embout \_ Set \_ MCI \_

Le message **WM \_ Cap \_ Set \_ MCI \_ Device** spécifie le nom du périphérique vidéo MCI à utiliser pour capturer les données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message stocke le nom du périphérique MCI dans une structure interne. Il n’ouvre pas ou n’accède pas à l’appareil. Le nom de périphérique par défaut est **null**.

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

 

 





