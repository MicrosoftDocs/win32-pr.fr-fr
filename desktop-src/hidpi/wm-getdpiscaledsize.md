---
title: Message WM_GETDPISCALEDSIZE (winuser. h)
description: Ce message indique au système d’exploitation que la fenêtre sera dimensionnée sur une dimension autre que la valeur par défaut.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE message haute résolution
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465402"
---
# <a name="wm_getdpiscaledsize-message"></a>\_Message WM GETDPISCALEDSIZE

Ce message indique au système d’exploitation que la fenêtre sera dimensionnée sur une dimension autre que la valeur par défaut.

Ce message est envoyé aux fenêtres de niveau supérieur avec un [ \_ \_ contexte de détection PPP](dpi-awareness-context.md) de par moniteur v2 avant l’envoi d’un message [**\_ DPICHANGED WM**](wm-dpichanged.md) et permet à la fenêtre de calculer sa taille souhaitée pour la modification de la valeur PPP en attente. Comme la mise à l’échelle PPP linéaire est le comportement par défaut, cela n’est utile que dans les scénarios où la fenêtre souhaite évoluer de manière non linéaire. Si l’application répond à ce message, la taille résultante sera le rectangle candidat envoyer à **WM \_ DPICHANGED**.

Utilisez ce message pour modifier la taille du Rect fourni avec [**WM \_ DPICHANGED**](wm-dpichanged.md).


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

WPARAM contient une valeur PPP. La taille de fenêtre mise à l’échelle que l’application doit définir doit être calculée comme si la fenêtre devait basculer vers cette PPP.

</dd> <dt>

*lParam* 
</dt> <dd>

Le LPARAM est un pointeur in/out vers une structure de taille. La \_ valeur de dans \_ le lParam correspond à la taille d’attente de la fenêtre après un déplacement initié par l’utilisateur ou un appel à [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si la fenêtre est redimensionnée, cette taille n’est pas nécessairement la même que la taille actuelle de la fenêtre au moment de la réception de ce message.

L' \_ \_ application doit écrire la valeur out dans lParam pour spécifier la taille de fenêtre mise à l’échelle souhaitée correspondant à la valeur DPI fournie dans wParam.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne une valeur BOOLÉENNE. Le retour de la valeur TRUE indique qu’une nouvelle taille a été calculée. Si la valeur renvoyée est FALSe, cela signifie que le message ne sera pas géré et que la mise à l’échelle PPP linéaire par défaut s’appliquera à la fenêtre.

## <a name="remarks"></a>Notes

Ce message est envoyé uniquement aux fenêtres de niveau supérieur qui ont un contexte de reconnaissance PPP de par moniteur v2.

Cet événement est nécessaire pour faciliter la mise à l’échelle non linéaire, et garantit que la position de Windows reste constante en relation avec le curseur et en cas de déplacement entre les moniteurs.

Il n’existe pas de gestion par défaut spécifique de ce message dans [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Comme pour tous les messages qu’il ne gère pas explicitement, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) retourne zéro pour ce message. Comme indiqué ci-dessus, ce retour indique au système d’utiliser le comportement linéaire par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

