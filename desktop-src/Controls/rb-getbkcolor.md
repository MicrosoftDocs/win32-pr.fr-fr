---
title: Message RB_GETBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan par défaut d’un contrôle rebar.
ms.assetid: be90d1ce-a1f8-446d-ae64-001f7174ab05
keywords:
- RB_GETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56e2b6c60076d878ddea275f5383f98c5a92ee868e00074c716c113382b7678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084999"
---
# <a name="rb_getbkcolor-message"></a>\_Message GETBKCOLOR RB

Récupère la couleur d’arrière-plan par défaut d’un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan par défaut actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETBKCOLOR RB**](rb-setbkcolor.md)
</dt> </dl>

 

