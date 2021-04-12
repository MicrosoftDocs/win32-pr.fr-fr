---
title: Message WM_CAP_DRIVER_CONNECT (VFW. h)
description: Le \_ message WM capuchon \_ Driver \_ Connect connecte une fenêtre de capture à un pilote de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- Message WM_CAP_DRIVER_CONNECT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384471"
---
# <a name="wm_cap_driver_connect-message"></a>\_Message de \_ connexion du pilote WM Cap \_

Le message **WM \_ capuchon \_ Driver \_ Connect** connecte une fenêtre de capture à un pilote de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Index du pilote de capture. L’index peut être compris entre 0 et 9.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si le pilote de capture spécifié ne peut pas être connecté à la fenêtre de capture.

## <a name="remarks"></a>Notes

La connexion d’un pilote de capture à une fenêtre de capture déconnecte automatiquement tout pilote de capture précédemment connecté.

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

 

 





