---
title: Message RB_GETBANDBORDERS (commctrl. h)
description: Récupère les bordures d’une bande. Le résultat de ce message peut être utilisé pour calculer la zone utilisable dans une bande.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS les contrôles de message Windows
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
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942460"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

