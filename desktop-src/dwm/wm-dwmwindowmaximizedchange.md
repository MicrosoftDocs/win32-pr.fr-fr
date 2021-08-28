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
ms.openlocfilehash: 93cfa4ac380b6ff439fb2bf4805846c0b774a90bcfdcd83673ead2334a3c7094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117749"
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

## <a name="remarks"></a>Remarques

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

