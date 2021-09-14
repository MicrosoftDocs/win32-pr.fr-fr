---
title: Message TTM_RELAYEVENT (commctrl. h)
description: Transmet un message de souris à un contrôle ToolTip pour traitement.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115826"
---
# <a name="ttm_relayevent-message"></a>\_Message atténuation RELAYEVENT

Transmet un message de souris à un contrôle ToolTip pour traitement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro. **Windows 7 et versions ultérieures :** Si la position de l’info-bulle est décalée par rapport à la position du curseur (dans le cas contraire, un doigt ou un dispositif de pointage n’est pas obstrué), ce paramètre peut contenir des informations supplémentaires extraites du message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Récupérez ces informations supplémentaires avec [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) qui contient le message à relayer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Un contrôle ToolTip traite uniquement les messages suivants qui lui sont passés par le message **atténuation \_ RELAYEVENT** :

-   \_LBUTTONDOWN WM
-   \_LBUTTONUP WM
-   \_MBUTTONDOWN WM
-   \_MBUTTONUP WM
-   WM \_ MOUSEMOVE
-   \_NCMOUSEMOVE WM
-   \_RBUTTONDOWN WM
-   \_RBUTTONUP WM

Tous les autres messages sont ignorés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

