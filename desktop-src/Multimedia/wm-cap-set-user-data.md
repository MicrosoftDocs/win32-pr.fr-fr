---
title: Message WM_CAP_SET_USER_DATA (VFW. h)
description: Le \_ message WM Cap \_ Set \_ User \_ Data associe une \_ valeur de données PTR longue à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- Message WM_CAP_SET_USER_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106108"
---
# <a name="wm_cap_set_user_data-message"></a>\_Message WM Cap \_ Set \_ User \_ Data

Le message **WM \_ Cap \_ Set \_ User \_ Data** associe une valeur de données **\_ ptr longue** à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

Valeur de données à associer à une fenêtre de capture.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu est en cours.

## <a name="remarks"></a>Notes

En général, ce message est utilisé pour pointer vers un bloc de données associé à une fenêtre de capture.

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

 

 





