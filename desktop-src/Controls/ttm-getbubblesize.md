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
ms.openlocfilehash: 8354a93521b6adac9306374f5bfbc99e84738ac87f0471a22f199b7b611f100b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769379"
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

## <a name="remarks"></a>Remarques

Si les \_ \_ indicateurs absolus Track et ttf sont définis dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle, ce message peut être utilisé pour aider à positionner l’info-bulle avec précision.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





