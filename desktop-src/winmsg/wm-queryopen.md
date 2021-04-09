---
description: Envoyé à une icône lorsque l’utilisateur demande que la fenêtre soit restaurée à sa taille et à sa position précédentes.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Message WM_QUERYOPEN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034531"
---
# <a name="wm_queryopen-message"></a>\_Message WM QUERYOPEN

Envoyé à une icône lorsque l’utilisateur demande que la fenêtre soit restaurée à sa taille et à sa position précédentes.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_QUERYOPEN                    0x0013
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

Si l’icône peut être ouverte, une application qui traite ce message doit retourner la **valeur true**; Sinon, elle doit retourner **false** pour empêcher l’ouverture de l’icône.

## <a name="remarks"></a>Notes

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la **valeur true**.

Lors du traitement de ce message, l’application ne doit effectuer aucune action qui entraînerait une modification de l’activation ou du focus (par exemple, la création d’une boîte de dialogue).

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

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
