---
title: MCN_SELECT le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque l’utilisateur effectue une sélection de date explicite dans un contrôle Month Calendar. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- Contrôles Windows de code de notification MCN_SELECT
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032491"
---
# <a name="mcn_select-notification-code"></a>MCN \_ Sélectionner un code de notification

Envoyé par un contrôle Month Calendar lorsque l’utilisateur effectue une sélection de date explicite dans un contrôle Month Calendar. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) qui contient des informations sur la plage de dates actuellement sélectionnée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le code de notification **\_ Select MCN** est similaire à [**MCN \_ selChange**](mcn-selchange.md), mais **MCN \_ Select** est envoyée uniquement en réponse aux sélections de dates explicites de l’utilisateur. **MCN \_ SELCHANGE** s’applique à toute modification de sélection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





