---
title: Message MCIWNDM_SETINACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM SETINACTIVETIMER définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est inactive. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- Message MCIWNDM_SETINACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508890"
---
# <a name="mciwndm_setinactivetimer-message"></a>\_Message MCIWNDM SETINACTIVETIMER

Le message **MCIWNDM \_ SETINACTIVETIMER** définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est inactive. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inactive*
</dt> <dd>

Période de mise à jour, en millisecondes. La valeur par défaut est 2000 millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





