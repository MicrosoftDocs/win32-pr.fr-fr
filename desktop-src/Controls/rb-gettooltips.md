---
title: Message RB_GETTOOLTIPS (commctrl. h)
description: Récupère le handle d’un contrôle ToolTip associé au contrôle rebar.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104437"
---
# <a name="rb_gettooltips-message"></a>\_Message GETTOOLTIPS RB

Récupère le handle d’un contrôle ToolTip associé au contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HWND** qui est le handle du contrôle ToolTip associé au contrôle rebar, ou zéro si aucun contrôle ToolTip n’est associé au contrôle rebar.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





