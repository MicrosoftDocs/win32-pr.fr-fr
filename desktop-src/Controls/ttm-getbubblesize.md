---
title: Message TTM_GETBUBBLESIZE (commctrl. h)
description: Retourne la largeur et la hauteur d’un contrôle ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115881"
---
# <a name="ttm_getbubblesize-message"></a>\_Message atténuation GETBUBBLESIZE

Retourne la largeur et la hauteur d’un contrôle ToolTip.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la largeur de l’info-bulle dans le mot de poids faible et la hauteur du mot haut en cas de réussite. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Si les \_ \_ indicateurs absolus Track et ttf sont définis dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle, ce message peut être utilisé pour aider à positionner l’info-bulle avec précision.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





