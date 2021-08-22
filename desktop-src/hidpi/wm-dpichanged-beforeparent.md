---
title: Message WM_DPICHANGED_BEFOREPARENT (winuser. h)
description: Pour les fenêtres de niveau supérieur par moniteur v2, ce message est envoyé à tous les HWND dans l’arborescence HWDN enfant de la fenêtre qui subit une modification PPP. | Message WM_DPICHANGED_BEFOREPARENT (winuser. h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT message haute résolution
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a52216052f597ce26e5be476a970ff78f0297c08124c9b1ca89453b6fca76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557669"
---
# <a name="wm_dpichanged_beforeparent-message"></a>\_ \_ Message BEFOREPARENT WM DPICHANGED

Pour les fenêtres de niveau supérieur [par moniteur v2](dpi-awareness-context.md) , ce message est envoyé à tous les HWND dans l’arborescence HWDN enfant de la fenêtre qui subit une modification PPP. Ce message s’affiche avant que la fenêtre de niveau supérieur ne reçoive le [**WM \_ DPICHANGED**](wm-dpichanged.md)et parcourt l’arborescence enfant du bas vers le haut.


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
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

## <a name="return-value"></a>Valeur retournée

Cette valeur n’est pas utilisée et est ignorée par le système.

## <a name="remarks"></a>Remarques

Il n’y a pas de gestion par défaut de ce message dans [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Ce message est envoyé uniquement lorsque la fenêtre de niveau supérieur a un contexte de sensibilisation en DPI de PMv2.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_DPICHANGED WM**](wm-dpichanged.md)
</dt> <dt>

[**\_DPICHANGED WM \_ AFTERPARENT**](wm-dpichanged-afterparent.md)
</dt> </dl>

 

