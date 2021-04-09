---
title: Message WM_CAP_GET_STATUS (VFW. h)
description: Le \_ message WM Cap \_ obtenir \_ l’État récupère l’état de la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- Message WM_CAP_GET_STATUS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032322"
---
# <a name="wm_cap_get_status-message"></a>Message d’état de l' \_ \_ extraction WM \_

Le message **WM \_ Cap obtenir l' \_ \_ État** récupère l’état de la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la structure référencée par **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*x*
</dt> <dd>

Pointeur vers une structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.

## <a name="remarks"></a>Notes

La structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contient l’état actuel de la fenêtre de capture. Étant donné que cet État est dynamique et change en réponse à différents messages, l’application doit initialiser cette structure après avoir envoyé le message [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (ou à l’aide de la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) et chaque fois qu’il doit activer les éléments de menu ou déterminer l’état réel de la fenêtre.

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

 

 





