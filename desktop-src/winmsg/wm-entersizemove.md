---
description: Envoyé une fois à une fenêtre après l’entrée dans la boucle modale de redimensionnement ou de déplacement.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Message WM_ENTERSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536177"
---
# <a name="wm_entersizemove-message"></a>\_Message WM ENTERSIZEMOVE

Envoyé une fois à une fenêtre après l’entrée dans la boucle modale de redimensionnement ou de déplacement. La fenêtre passe à la boucle modale de déplacement ou de redimensionnement quand l’utilisateur clique sur la barre de titre ou la bordure de redimensionnement de la fenêtre, ou lorsque la fenêtre passe le message [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) et que le paramètre *wParam* du message spécifie la valeur **SC \_ Move** ou **SC \_ Size** . L’opération est terminée quand [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne.

Le système envoie le message **WM \_ ENTERSIZEMOVE** , que le glissement de fenêtres entières soit activé ou non.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner zéro si elle traite ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_EXITSIZEMOVE WM**](wm-exitsizemove.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](../menurc/wm-syscommand.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
