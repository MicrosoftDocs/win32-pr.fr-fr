---
title: Message TCM_INSERTITEM (commctrl. h)
description: Insère un nouvel onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM les contrôles de message Windows
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
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517321"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TCM \_ INSERTITEMW** (Unicode) et **TCM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





