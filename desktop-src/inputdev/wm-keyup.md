---
title: Message WM_KEYUP (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’une touche non-système est relâchée. Une touche non-système est une touche qui est enfoncée lorsque la touche ALT n’est pas enfoncée ou une touche du clavier qui est enfoncée lorsqu’une fenêtre a le focus clavier.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc23b941f232007a781ca160538f28d864f818639df47a180de472f54cd89a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247821"
---
# <a name="wm_keyup-message"></a>\_Message WM KEYUP

Publié dans la fenêtre qui a le focus clavier lorsqu’une touche non-système est relâchée. Une touche non-système est une touche qui est enfoncée lorsque la touche ALT n’est *pas* enfoncée ou une touche du clavier qui est enfoncée lorsqu’une fenêtre a le focus clavier.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de la clé virtuelle de la clé non-système. Consultez [codes de clé virtuelle](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.



| Bits  | Signification                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions du message en cours. La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée. Le nombre de répétitions est toujours 1 pour un message **WM \_ KEYUP** . |
| 16-23 | Code d’analyse. La valeur dépend du fabricant d’ordinateurs OEM.                                                                                                                                                                     |
| 24    | Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches. La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.         |
| 25-28 | Réservé n’utilisez pas.                                                                                                                                                                                            |
| 29    | Code de contexte. La valeur est toujours 0 pour un message **WM \_ KEYUP** .                                                                                                                                             |
| 30    | État de la clé précédente. La valeur est toujours 1 pour un message **WM \_ KEYUP** .                                                                                                                                       |
| 31    | État de transition. La valeur est toujours 1 pour un message **WM \_ KEYUP** .                                                                                                                                         |

Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre de niveau supérieur si la touche F10 ou la touche Alt a été relâchée. Le paramètre *wParam* du message est défini sur SC \_ keymenu.

Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .

Les applications doivent passer *wParam* à [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sans aucune modification.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM- \_ touche**](wm-keydown.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

