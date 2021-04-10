---
title: Message TTM_GETBUBBLESIZE (commctrl. h)
description: Retourne la largeur et la hauteur d’un contrôle ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103750"
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

## <a name="return-value"></a>Valeur retournée

Retourne la largeur de l’info-bulle dans le mot de poids faible et la hauteur du mot haut en cas de réussite. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Si les \_ \_ indicateurs absolus Track et ttf sont définis dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle, ce message peut être utilisé pour aider à positionner l’info-bulle avec précision.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





