---
title: Message WM_DWMNCRENDERINGCHANGED (winuser. h)
description: Envoyé lorsque la stratégie de rendu de la zone non cliente a changé.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- Message de WM_DWMNCRENDERINGCHANGED Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcae8595315d43737d88d6a302bcac3a328418abd19d77b96bd13ee5ef66496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502652"
---
# <a name="wm_dwmncrenderingchanged-message"></a>\_Message WM DWMNCRENDERINGCHANGED

Envoyé lorsque la stratégie de rendu de la zone non cliente a changé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie si le rendu DWM est activé pour la zone non cliente de la fenêtre. **True** si l’option est activée ; Sinon, **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

Les fonctions [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) et [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) sont utilisées pour récupérer ou définir la stratégie de rendu non client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

