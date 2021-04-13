---
title: Message RB_GETBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan par défaut d’un contrôle rebar.
ms.assetid: be90d1ce-a1f8-446d-ae64-001f7174ab05
keywords:
- RB_GETBKCOLOR les contrôles de message Windows
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
ms.openlocfilehash: 7bb0c6f2348dfa54dc02ddc40658fd1289885ff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466079"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETBKCOLOR RB**](rb-setbkcolor.md)
</dt> </dl>

 

