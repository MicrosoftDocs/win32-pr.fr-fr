---
title: Message WM_DWMCOMPOSITIONCHANGED (winuser. h)
description: Informe toutes les fenêtres de niveau supérieur qui Gestionnaire de fenêtrage composition (DWM) ont été activées ou désactivées.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- Message de WM_DWMCOMPOSITIONCHANGED Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012658"
---
# <a name="wm_dwmcompositionchanged-message"></a>\_Message WM DWMCOMPOSITIONCHANGED

Informe toutes les fenêtres de niveau supérieur qui Gestionnaire de fenêtrage composition (DWM) ont été activées ou désactivées.

> [!Note]  
> à partir de Windows 8, la composition DWM est toujours activée. ce message n’est donc pas envoyé, quelles que soient les modifications du mode vidéo.

 

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

La fonction [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) peut être utilisée pour déterminer l’état actuel de la composition.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

