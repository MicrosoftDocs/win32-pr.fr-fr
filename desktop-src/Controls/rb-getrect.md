---
title: Message RB_GETRECT (commctrl. h)
description: Récupère le rectangle englobant pour une bande donnée dans un contrôle rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- RB_GETRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d2f085fa7c6f413700156999f1325879f91affc2c8984fb33d08cb6cc90b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169295"
---
# <a name="rb_getrect-message"></a>\_Message GETRECT RB

Récupère le rectangle englobant pour une bande donnée dans un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro d’une bande dans le contrôle rebar.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les limites de la bande rebar.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

