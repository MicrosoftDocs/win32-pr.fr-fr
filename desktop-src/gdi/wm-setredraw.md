---
description: Une application envoie le \_ message WM SETREDRAW à une fenêtre pour autoriser le rafraîchissement des modifications apportées à cette fenêtre ou empêcher le rafraîchissement des modifications apportées à cette fenêtre.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Message WM_SETREDRAW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203877"
---
# <a name="wm_setredraw-message"></a>\_Message WM SETREDRAW

Une application envoie le message **WM \_ SETREDRAW** à une fenêtre pour autoriser le rafraîchissement des modifications apportées à cette fenêtre ou empêcher le rafraîchissement des modifications apportées à cette fenêtre.

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

<dl> <dt>

*wParam* 
</dt> <dd>

État du redessin. Si ce paramètre a la **valeur true**, le contenu peut être redessiné après une modification. Si ce paramètre a la **valeur false**, le contenu ne peut pas être redessiné après une modification.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application retourne la valeur zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Ce message peut être utile si une application doit ajouter plusieurs éléments à une zone de liste. L’application peut appeler ce message avec *wParam* défini sur **false**, ajouter les éléments, puis appeler à nouveau le message avec *wParam* défini sur **true**. Enfin, l’application peut appeler [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, RDW \_ Erase \| RDW \_ frame \| RDW non \_ valide \| RDW \_ ALLCHILDREN) pour provoquer la redessination de la zone de liste.

> [!Note]  
> [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) avec les indicateurs spécifiés est utilisé à la place de [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , car le premier est nécessaire pour certains contrôles qui ont eux-mêmes une zone non cliente, ou qui ont des styles de fenêtre qui les empêchent de recevoir une zone non cliente (par exemple, **WS \_ THICKFRAME**, **WS \_ Border** ou **WS \_ ex \_ CLIENTEDGE**). Si le contrôle n’a pas de zone non cliente, **RedrawWindow** avec ces indicateurs n’effectuera qu’un maximum d’invalidation, comme le ferait **InvalidateRect** .

 

Si l’application envoie le message **WM \_ SETREDRAW** à une fenêtre masquée, la fenêtre devient visible (autrement dit, le système d’exploitation ajoute le style **WS \_ visible** à la fenêtre).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble de la peinture et du dessin](painting-and-drawing.md)
</dt> <dt>

[Peinture et dessin de messages](painting-and-drawing-messages.md)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
