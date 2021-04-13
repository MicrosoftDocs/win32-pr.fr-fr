---
title: Message WM_DWMWINDOWMAXIMIZEDCHANGE (winuser. h)
description: Envoyé lorsqu’une fenêtre composée de Gestionnaire de fenêtrage (DWM) est agrandie.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Message de WM_DWMWINDOWMAXIMIZEDCHANGE Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384732"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a>\_Message WM DWMWINDOWMAXIMIZEDCHANGE

Envoyé lorsqu’une fenêtre composée de Gestionnaire de fenêtrage (DWM) est agrandie.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Affectez la valeur true pour spécifier que la fenêtre a été agrandie.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

