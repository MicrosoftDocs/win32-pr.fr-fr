---
title: Message WM_SYSKEYDOWN (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur appuie sur la touche F10 (qui active la barre de menus) ou maintient la touche ALT enfoncée, puis appuie sur une autre touche.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1398d843711e868a6b5b96cf6a66893bf74fef1e50bfdd61fa36f81f05c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611319"
---
# <a name="wm_syskeydown-message"></a>\_Message WM SYSKEYDOWN

Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur appuie sur la touche F10 (qui active la barre de menus) ou maintient la touche ALT enfoncée, puis appuie sur une autre touche. Elle se produit également lorsqu’aucune fenêtre n’a actuellement le focus clavier. dans ce cas, le message **WM \_ SYSKEYDOWN** est envoyé à la fenêtre active. La fenêtre qui reçoit le message peut faire la distinction entre ces deux contextes en vérifiant le code de contexte dans le paramètre *lParam* .


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de la touche virtuelle de la touche enfoncée. Consultez [**codes de clé virtuelle**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.



| Bits  | Signification                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions du message en cours. La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée. Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés. Toutefois, le nombre de répétitions n’est pas cumulatif. |
| 16-23 | Code d’analyse. La valeur dépend du fabricant d’ordinateurs OEM.                                                                                                                                                                                                                          |
| 24    | Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches. La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.                                                              |
| 25-28 | Réservé n’utilisez pas.                                                                                                                                                                                                                                                 |
| 29    | Code de contexte. La valeur est 1 si la touche ALT est enfoncée pendant que la touche est enfoncée ; elle est égale à 0 si le message **\_ SYSKEYDOWN WM** est publié dans la fenêtre active, car aucune fenêtre n’a le focus clavier.                                                                  |
| 30    | État de la clé précédente. La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.                                                                                                                                                    |
| 31    | État de transition. La valeur est toujours 0 pour un message **WM \_ SYSKEYDOWN** .                                                                                                                                                                                         |

Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examine la clé spécifiée et génère un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) si la clé est de type Tab ou entrée.

Lorsque le code de contexte est égal à zéro, le message peut être passé à la fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , qui le gère comme s’il s’agissait d’un message de clé normal au lieu d’un message de touche de caractère. Cela permet d’utiliser les touches d’accès rapide avec la fenêtre active, même si la fenêtre active n’a pas le focus clavier.

En raison de la répétition automatique, plusieurs messages **WM \_ SYSKEYDOWN** peuvent se produire avant l’envoi d’un message [**\_ SYSKEYUP WM**](wm-syskeyup.md) . L’état de clé précédent (bit 30) peut être utilisé pour déterminer si le message **WM \_ SYSKEYDOWN** indique la première transition vers le haut ou une transition répétée.

Pour les claviers à touche 101 et 102 améliorés, les touches améliorées sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .

Ce message est également envoyé chaque fois que l’utilisateur appuie sur la touche F10 sans la touche ALT.

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

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**\_SYSKEYUP WM**](wm-syskeyup.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

