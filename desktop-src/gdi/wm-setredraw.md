---
description: Vous envoyez le message **WM_SETREDRAW** à une fenêtre pour autoriser le rafraîchissement des modifications de cette fenêtre, ou pour empêcher que les modifications apportées à cette fenêtre soient redessinées.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Message WM_SETREDRAW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593455"
---
# <a name="wm_setredraw-message"></a>Message WM_SETREDRAW

Vous envoyez le message **WM \_ SETREDRAW** à une fenêtre pour que les modifications apportées à cette fenêtre soient redessinées ou pour empêcher que les modifications apportées à cette fenêtre soient redessinées.

Pour envoyer ce message, appelez la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec les paramètres suivants.

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a>Paramètres

`wParam`

État du redessin. Si ce paramètre a la **valeur true**, le contenu peut être redessiné après une modification. Si ce paramètre a la **valeur false**, le contenu ne peut pas être redessiné après une modification.

`lParam`

Ce paramètre n’est pas utilisé.

## <a name="return-value"></a>Valeur renvoyée

Votre application doit retourner 0 si elle traite ce message.

## <a name="remarks"></a>Notes

Ce message peut être utile si votre application doit ajouter plusieurs éléments à une zone de liste. Votre application peut appeler ce message avec *wParam* défini sur **false**, ajouter les éléments, puis appeler à nouveau le message avec *wParam* défini sur **true**. Enfin, votre application peut appeler [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, RDW \_ Erase \| RDW \_ frame \| RDW non \_ valide \| RDW \_ ALLCHILDREN) pour provoquer la redessination de la zone de liste.

> [!NOTE] 
> Vous devez utiliser [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) avec les indicateurs spécifiés, au lieu de [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), car le premier est nécessaire pour certains contrôles qui ont eux-mêmes une zone non cliente, ou qui ont des styles de fenêtre qui les empêchent de recevoir une zone non cliente (par exemple **WS_THICKFRAME**, **WS_BORDER** ou **WS_EX_CLIENTEDGE**). Si le contrôle n’a pas de zone non cliente, les **RedrawWindow** avec ces indicateurs effectuent uniquement la même invalidation que le nombre de **InvalidateRect** .

La transmission d’un message **WM_SETREDRAW** à la fonction **DefWindowProc** supprime le style **WS_VISIBLE** de la fenêtre lorsque *wParam* a la valeur **false**. Bien que le contenu de la fenêtre reste visible à l’écran, la fonction [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) retourne la **valeur false** lorsqu’elle est appelée sur une fenêtre dans cet État. 

La transmission d’un message **WM_SETREDRAW** à la fonction **DefWindowProc** ajoute le style **WS_VISIBLE** à la fenêtre, s’il n’est pas défini, lorsque *wParam* a la valeur **true**. Si votre application envoie le message d' **WM_SETREDRAW** avec *wParam* défini sur **true** dans une fenêtre masquée, la fenêtre devient visible. 

**Windows 10 et versions ultérieures ; Windows Server 2016 et versions ultérieures**. Le système définit une propriété nommée *SysSetRedraw* dans une fenêtre dont la procédure de fenêtre transmet **WM_SETREDRAW** messages à **DefWindowProc**. Vous pouvez utiliser la fonction [**getprop**](/windows/win32/api/Winuser/nf-winuser-getpropa) pour récupérer la valeur de la propriété lorsqu’elle est disponible. **Getprop** retourne une valeur différente de zéro quand redessin est désactivé. **Getprop** retourne zéro lorsque redessin est activé, ou lorsque la propriété de fenêtre n’existe pas. 

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Windows 2000 Professionnel - \[Applications de bureau uniquement\] |
| Serveur minimal pris en charge | Windows 2000 Server - \[Applications de bureau uniquement\] |
| En-tête | <dl><dt>Winuser. h (inclure Windows. h)</dt></dl> |

## <a name="see-also"></a>Voir aussi

* [Vue d’ensemble de la peinture et du dessin](painting-and-drawing.md)
* [Peinture et dessin de messages](painting-and-drawing-messages.md)
* [RedrawWindow](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
