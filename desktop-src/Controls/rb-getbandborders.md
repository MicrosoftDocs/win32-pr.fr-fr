---
title: Message RB_GETBANDBORDERS (commctrl. h)
description: Récupère les bordures d’une bande. Le résultat de ce message peut être utilisé pour calculer la zone utilisable dans une bande.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6b07303c10ef6f466907b11cf0e100927f63480690e77ac3dcbe80df80af97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409711"
---
# <a name="rb_getbandborders-message"></a>\_Message GETBANDBORDERS RB

Récupère les bordures d’une bande. Le résultat de ce message peut être utilisé pour calculer la zone utilisable dans une bande.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la bande pour laquelle les bordures seront récupérées.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur désignant une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les bordures de la bande. Si le contrôle rebar a le style [**RBS \_ BANDBORDERS**](rebar-control-styles.md) , chaque membre de cette structure recevra le nombre de pixels, sur le côté correspondant de la bande, qui constituent la bordure. Si le contrôle rebar n’a pas le style **RBS \_ BANDBORDERS** , seul le membre de **gauche** de cette structure reçoit des informations valides.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

