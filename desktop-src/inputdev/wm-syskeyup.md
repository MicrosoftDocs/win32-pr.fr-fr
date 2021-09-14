---
title: Message WM_SYSKEYUP (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur relâche une touche qui a été enfoncée alors que la touche ALT était maintenue enfoncée.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192136"
---
# <a name="wm_syskeyup-message"></a>\_Message WM SYSKEYUP

Publié dans la fenêtre qui a le focus clavier lorsque l’utilisateur relâche une touche qui a été enfoncée alors que la touche ALT était maintenue enfoncée. Elle se produit également lorsqu’aucune fenêtre n’a actuellement le focus clavier. dans ce cas, le message **WM \_ SYSKEYUP** est envoyé à la fenêtre active. La fenêtre qui reçoit le message peut faire la distinction entre ces deux contextes en vérifiant le code de contexte dans le paramètre *lParam* .

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de la touche virtuelle de la touche en cours de publication. Consultez [**codes de clé virtuelle**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.



| Bits  | Signification                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions du message en cours. La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée. Le compteur REPEAT est toujours un pour un message **WM \_ SYSKEYUP** .         |
| 16-23 | Code d’analyse. La valeur dépend du fabricant d’ordinateurs OEM.                                                                                                                                                                                  |
| 24    | Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches. La valeur est 1 s’il s’agit d’une clé étendue ; dans le cas contraire, il est égal à zéro.                   |
| 25-28 | Réservé n’utilisez pas.                                                                                                                                                                                                         |
| 29    | Code de contexte. La valeur est 1 si la touche ALT est enfoncée pendant que la touche est relâchée ; elle est égale à zéro si le message **\_ SYSKEYUP WM** est publié dans la fenêtre active, car aucune fenêtre n’a le focus clavier. |
| 30    | État de la clé précédente. La valeur est toujours 1 pour un message **WM \_ SYSKEYUP** .                                                                                                                                                 |
| 31    | État de transition. La valeur est toujours 1 pour un message **WM \_ SYSKEYUP** .                                                                                                                                                   |

Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre de niveau supérieur si la touche F10 ou la touche Alt a été relâchée. Le paramètre *wParam* du message est défini sur **SC \_ keymenu**.

Lorsque le code de contexte est égal à zéro, le message peut être passé à la fonction [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , qui le gère comme s’il s’agissait d’un message de clé normal au lieu d’un message de touche de caractère. Cela permet d’utiliser les touches d’accès rapide avec la fenêtre active, même si la fenêtre active n’a pas le focus clavier.

Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .

Pour les non-U. S. clavier amélioré 102 touches, la touche ALT de droite est gérée comme une touche CTRL + ALT. Le tableau suivant présente la séquence de messages qui se produit lorsque l’utilisateur appuie sur cette touche et la relâche.



| Message                           | Code de la touche virtuelle |
|-----------------------------------|------------------|
| [**WM- \_ touche**](wm-keydown.md) | **\_contrôle VK**  |
| [**WM- \_ touche**](wm-keydown.md) | **\_menu VK**     |
| [**WM \_ KEYUP**](wm-keyup.md)     | **\_contrôle VK**  |
| **\_SYSKEYUP WM**                  | **\_menu VK**     |



 

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

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**\_SYSKEYDOWN WM**](wm-syskeydown.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

