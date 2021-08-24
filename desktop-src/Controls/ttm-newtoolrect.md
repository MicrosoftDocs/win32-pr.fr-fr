---
title: Message TTM_NEWTOOLRECT (commctrl. h)
description: Définit un nouveau rectangle englobant pour un outil.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13889b0e9c0d80392b88130c33e5e9723ceb776a60a6b941d205d514d96ca22f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750979"
---
# <a name="ttm_newtoolrect-message"></a>\_Message atténuation NEWTOOLRECT

Définit un nouveau rectangle englobant pour un outil.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Les membres **HWND** et **UID** identifient un outil, tandis que le membre **Rect** spécifie le nouveau rectangle englobant. Le membre **cbSize** de cette structure doit être rempli avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ NEWTOOLRECTW** (Unicode) et **atténuation \_ NEWTOOLRECTA** (ANSI)<br/>           |



 

 





