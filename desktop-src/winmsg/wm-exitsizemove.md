---
description: Envoyé une fois à une fenêtre, après la sortie de la boucle modale de redimensionnement ou de déplacement.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Message WM_EXITSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541867"
---
# <a name="wm_exitsizemove-message"></a>\_Message WM EXITSIZEMOVE

Envoyé une fois à une fenêtre, après la sortie de la boucle modale de redimensionnement ou de déplacement. La fenêtre entre dans la boucle modale de déplacement ou de redimensionnement lorsque l’utilisateur clique sur la barre de titre ou la bordure de redimensionnement de la fenêtre, ou lorsque la fenêtre passe le message [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) et que le paramètre *wParam* du message spécifie la valeur de la **\_ taille** de **SC \_ MOV** E ou SC. L’opération est terminée quand [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_EXITSIZEMOVE                 0x0232
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

[**\_ENTERSIZEMOVE WM**](wm-entersizemove.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
