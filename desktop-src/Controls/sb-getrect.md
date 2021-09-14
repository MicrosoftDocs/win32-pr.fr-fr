---
title: Message SB_GETRECT (commctrl. h)
description: Récupère le rectangle englobant d’un composant dans une fenêtre d’État.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- SB_GETRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117093"
---
# <a name="sb_getrect-message"></a>\_Message SB GETRECT

Récupère le rectangle englobant d’un composant dans une fenêtre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro du composant dont le rectangle englobant doit être récupéré.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

