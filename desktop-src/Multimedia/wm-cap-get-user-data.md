---
title: Message WM_CAP_GET_USER_DATA (VFW. h)
description: Le \_ message WM Cap \_ obtenir des \_ \_ données utilisateur récupère une \_ valeur de données PTR longue associée à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- Message WM_CAP_GET_USER_DATA Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509146"
---
# <a name="wm_cap_get_user_data-message"></a>\_Message d' \_ extraction \_ de \_ données utilisateur de l’embout WM

Le message **WM \_ Cap obtenir des \_ \_ \_ données utilisateur** récupère une valeur de données **\_ ptr longue** associée à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur enregistrée précédemment à l’aide du message [**WM \_ embout \_ Set \_ User \_ Data**](wm-cap-set-user-data.md) .

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

 

 





