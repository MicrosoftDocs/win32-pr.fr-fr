---
description: Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan est sur le point de changer à la suite d’un appel à la fonction SetWindowPos ou à une autre fonction de gestion de fenêtre.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Message WM_WINDOWPOSCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219729"
---
# <a name="wm_windowposchanging-message"></a>\_Message WM WINDOWPOSCHANGING

Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan est sur le point de changer à la suite d’un appel à la fonction [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou à une autre fonction de gestion de fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) qui contient des informations sur les nouvelles taille et position de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Pour une fenêtre avec le [**style \_ WS Overlapped**](window-styles.md) ou **WS \_ THICKFRAME** , la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie le message [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) à la fenêtre. Cela permet de valider la nouvelle taille et la position de la fenêtre et d’appliquer les styles du client [cs \_ BYTEALIGNCLIENT](about-window-classes.md) et CS \_ BYTEALIGNWINDOW. Si vous ne transmettez pas le message **WM \_ WINDOWPOSCHANGING** à la fonction **DefWindowProc** , une application peut remplacer ces valeurs par défaut.

Pendant le traitement de ce message, la modification de l’une des valeurs dans [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affecte la nouvelle taille, la position ou l’emplacement de la fenêtre dans l’ordre de plan. Une application peut empêcher les modifications apportées à la fenêtre en définissant ou en effaçant les bits appropriés dans le membre **Flags** de **WINDOWPOS**.

## <a name="requirements"></a>Spécifications



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

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**\_GETMINMAXINFO WM**](wm-getminmaxinfo.md)
</dt> <dt>

[**déplacement de WM \_**](wm-move.md)
</dt> <dt>

[**taille du WM \_**](wm-size.md)
</dt> <dt>

[**\_WINDOWPOSCHANGED WM**](wm-windowposchanged.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
