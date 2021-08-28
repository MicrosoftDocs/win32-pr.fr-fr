---
description: Envoyé une fois à une fenêtre après l’entrée dans la boucle modale de redimensionnement ou de déplacement.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Message WM_ENTERSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffbd3ac8c65b68998a37e64df2593c183b61adb3f8eba1fa140251174b503d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436254"
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

 

 
