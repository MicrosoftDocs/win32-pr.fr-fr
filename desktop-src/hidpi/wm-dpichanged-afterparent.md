---
title: Message WM_DPICHANGED_AFTERPARENT (winuser. h)
description: Pour les fenêtres de niveau supérieur par moniteur v2, ce message est envoyé à tous les HWND dans l’arborescence HWDN enfant de la fenêtre qui subit une modification PPP. | Message WM_DPICHANGED_AFTERPARENT (winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT message haute résolution
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120202"
---
# <a name="wm_dpichanged_afterparent-message"></a>\_ \_ Message AFTERPARENT WM DPICHANGED

Pour les fenêtres de niveau supérieur [par moniteur v2](dpi-awareness-context.md) , ce message est envoyé à tous les HWND dans l’arborescence HWDN enfant de la fenêtre qui subit une modification PPP. Ce message se produit une fois que la fenêtre de niveau supérieur reçoit le [**\_ DPICHANGED WM**](wm-dpichanged.md)et parcourt l’arborescence enfant du haut vers le haut.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Cette valeur n’est pas utilisée et sera égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Cette valeur n’est pas utilisée et sera égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette valeur n’est pas utilisée et est ignorée par le système.

## <a name="remarks"></a>Notes

Il n’y a pas de gestion par défaut de ce message dans [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Ce message est envoyé uniquement lorsque la fenêtre de niveau supérieur a un contexte de sensibilisation en DPI de PMv2.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_DPICHANGED WM**](wm-dpichanged.md)
</dt> <dt>

[**\_DPICHANGED WM \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

