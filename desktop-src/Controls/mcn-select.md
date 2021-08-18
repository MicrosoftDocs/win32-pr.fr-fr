---
title: MCN_SELECT le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque l’utilisateur effectue une sélection de date explicite dans un contrôle Month Calendar. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT les contrôles de Windows de code de notification
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
ms.openlocfilehash: 3e71674ebccd9a896a92f701e65c7767866b64edac25208248f4683792b5261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018967"
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

## <a name="remarks"></a>Remarques

Le code de notification **\_ Select MCN** est similaire à [**MCN \_ selChange**](mcn-selchange.md), mais **MCN \_ Select** est envoyée uniquement en réponse aux sélections de dates explicites de l’utilisateur. **MCN \_ SELCHANGE** s’applique à toute modification de sélection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





