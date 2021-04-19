---
description: Envoyé à une fenêtre lorsque sa zone non cliente doit être modifiée pour indiquer un état actif ou inactif.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Message WM_NCACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518694"
---
# <a name="wm_ncactivate-message"></a>\_Message WM NCACTIVATE

Envoyé à une fenêtre lorsque sa zone non cliente doit être modifiée pour indiquer un état actif ou inactif.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique quand une barre de titre ou une icône doit être modifiée pour indiquer un état actif ou inactif. Si une barre de titre ou une icône active doit être dessinée, le paramètre *wParam* a la **valeur true**. Si une barre de titre ou une icône inactive doit être dessinée, *wParam* a la **valeur false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Quand un [style visuel](../controls/themes-overview.md) est actif pour cette fenêtre, ce paramètre n’est pas utilisé.

Quand un style visuel n’est pas actif pour cette fenêtre, ce paramètre est un handle vers une région de mise à jour facultative pour la zone non cliente de la fenêtre. Si ce paramètre a la valeur-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ne redessine pas la zone non cliente pour refléter le changement d’État.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Lorsque le paramètre *wParam* a la **valeur false**, une application doit retourner **true** pour indiquer que le système doit procéder au traitement par défaut, ou retourner la valeur **false** pour empêcher la modification. Lorsque *wParam* a la valeur **true**, la valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Le traitement des messages liés à la zone non cliente d’une fenêtre standard n’est pas recommandé, car l’application doit être en mesure de dessiner toutes les parties requises de la zone non cliente pour la fenêtre. Si une application traite ce message, elle doit retourner la **valeur true** pour indiquer au système d’effectuer la modification de la fenêtre active. Si la fenêtre est réduite lorsque ce message est reçu, l’application doit transmettre le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dessine la barre de titre ou le titre de l’icône dans ses couleurs actives lorsque le paramètre *wParam* a la **valeur true** et dans ses couleurs inactives lorsque *wParam* a la **valeur false**.

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

 

 
