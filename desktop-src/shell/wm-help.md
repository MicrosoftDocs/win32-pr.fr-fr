---
description: Indique que l’utilisateur a appuyé sur la touche F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Message WM_HELP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95f1573888d378a8a60d2e6cef08581600a5f0526ab40675eb0ce7d9d0d0a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941099"
---
# <a name="wm_help-message"></a>\_Message d’aide WM

Indique que l’utilisateur a appuyé sur la touche F1. Si un menu est actif lorsque la touche F1 est enfoncée, l' **\_ aide WM** est envoyée à la fenêtre associée au menu ; sinon, l' **\_ aide WM** est envoyée à la fenêtre qui a le focus clavier. Si aucune fenêtre n’a le focus clavier, l' **\_ aide WM** est envoyée à la fenêtre actuellement active.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lphi* 
</dt> <dd>

Adresse d’une structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) qui contient des informations sur l’élément de menu, le contrôle, la boîte de dialogue ou la fenêtre pour laquelle l’aide est demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

## <a name="remarks"></a>Remarques

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) transmet **l' \_ aide WM** à la fenêtre parente d’une fenêtre enfant ou au propriétaire d’une fenêtre de niveau supérieur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 
