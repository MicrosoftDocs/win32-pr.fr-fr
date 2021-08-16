---
title: Message TCM_INSERTITEM (commctrl. h)
description: Insère un nouvel onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c3c17714218562d7ddc82497a7ef27e131e30a2ff04daf36970dfbcf5cc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829100"
---
# <a name="tcm_insertitem-message"></a>\_Message INSERTITEM de TCM

Insère un nouvel onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index du nouvel onglet.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) qui spécifie les attributs de l’onglet. Les membres **dwState** et **dwStateMask** de cette structure sont ignorés par ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index du nouvel onglet en cas de réussite, ou-1 dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TCM \_ INSERTITEMW** (Unicode) et **TCM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





