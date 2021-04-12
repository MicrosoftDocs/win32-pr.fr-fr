---
description: Envoyé à une fenêtre réduite (sous forme).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Message WM_QUERYDRAGICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319209"
---
# <a name="wm_querydragicon-message"></a>\_Message WM QUERYDRAGICON

Envoyé à une fenêtre réduite (sous forme). La fenêtre va être déplacée par l’utilisateur mais n’a pas d’icône définie pour sa classe. Une application peut retourner un handle à une icône ou un curseur. Le système affiche ce curseur ou cette icône lorsque l’utilisateur fait glisser l’icône.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_QUERYDRAGICON                0x0037
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

Une application doit retourner un handle à un curseur ou une icône que le système doit afficher lorsque l’utilisateur fait glisser l’icône. Le curseur ou l’icône doit être compatible avec la résolution du pilote d’affichage. Si l’application retourne la **valeur null**, le système affiche le curseur par défaut.

## <a name="remarks"></a>Notes

Quand l’utilisateur fait glisser l’icône d’une fenêtre sans icône de classe, le système remplace l’icône par un curseur par défaut. Si l’application requiert un curseur différent pour être affichée pendant le déplacement, elle doit retourner un handle au curseur ou à une icône compatible avec la résolution du pilote d’affichage. Si une application retourne un handle à un curseur ou une icône de couleur, le système convertit le curseur ou l’icône en noir et blanc. L’application peut appeler la fonction [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) ou [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) pour charger un curseur ou une icône à partir des ressources dans son fichier exécutable (. exe) et pour récupérer ce handle.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement. La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) est ignorée.

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

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
