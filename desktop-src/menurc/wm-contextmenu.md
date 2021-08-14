---
title: Message WM_CONTEXTMENU (winuser. h)
description: Avertit une fenêtre que l’utilisateur a cliqué avec le bouton droit de la souris (cliquez avec le bouton droit) dans la fenêtre.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c036bf0711f208bae25657d572102a7f4d82525076ee1d0b6f4ebd6598e8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472504"
---
# <a name="wm_contextmenu-message"></a>\_Message WM CONTEXTMENU

Avertit une fenêtre que l’utilisateur souhaite afficher un menu contextuel.  Il se peut que l’utilisateur ait cliqué sur le bouton droit de la souris (clic droit) dans la fenêtre, appuyé sur MAJ + F10 ou appuyé sur la touche applications (touche de menu contextuel) disponible sur certains claviers.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers la fenêtre dans laquelle l’utilisateur a cliqué avec le bouton droit de la souris. Il peut s’agir d’une fenêtre enfant de la fenêtre recevant le message. Pour plus d’informations sur le traitement de ce message, consultez la section Notes.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la position horizontale du curseur, en coordonnées d’écran, au moment du clic de la souris.

Le mot de poids fort spécifie la position verticale du curseur, en coordonnées d’écran, au moment du clic de la souris.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Une fenêtre peut traiter ce message en affichant un menu contextuel à l’aide des fonctions [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) ou [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Pour obtenir les positions horizontale et verticale, utilisez le code suivant.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Si une fenêtre n’affiche pas de menu contextuel, elle doit transmettre ce message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Si une fenêtre est une fenêtre enfant, **DefWindowProc** envoie le message au parent. Sinon, **DefWindowProc** affiche un menu contextuel par défaut si la position spécifiée se trouve dans la légende de la fenêtre.

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) génère le message **WM \_ CONTEXTMENU** lorsqu’il traite le [**message \_ WM RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) ou [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) ou lorsque l’utilisateur tape Shift + F10. Le message **WM \_ CONTEXTMENU** est également généré quand l’utilisateur appuie sur la touche [**VK \_ apps**](/windows/desktop/inputdev/virtual-key-codes) et la libère.

Si le menu contextuel est généré à partir du clavier, par exemple, si l’utilisateur tape MAJ + F10, les coordonnées x et y sont-1 et que l’application doit afficher le menu contextuel à l’emplacement de la sélection actuelle plutôt qu’à (xPos, yPos).

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

[**Obtient \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**Obtient \_ le \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**\_NCRBUTTONUP WM**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**\_RBUTTONUP WM**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

