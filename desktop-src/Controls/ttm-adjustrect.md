---
title: Message TTM_ADJUSTRECT (commctrl. h)
description: Calcule le rectangle d’affichage du texte d’un contrôle ToolTip à partir du rectangle de la fenêtre, ou le rectangle de la fenêtre d’info-bulle nécessaire pour afficher un rectangle d’affichage de texte spécifié.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115894"
---
# <a name="ttm_adjustrect-message"></a>\_Message atténuation ADJUSTRECT

Calcule le rectangle d’affichage du texte d’un contrôle ToolTip à partir du rectangle de la fenêtre, ou le rectangle de la fenêtre d’info-bulle nécessaire pour afficher un rectangle d’affichage de texte spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur qui spécifie l’opération à effectuer. Si la **valeur est true**, *lParam* est utilisé pour spécifier un rectangle d’affichage de texte et reçoit le rectangle de fenêtre correspondant. Si la **valeur est false**, *lParam* est utilisé pour spécifier un rectangle de fenêtre et reçoit le rectangle d’affichage de texte correspondant.

</dd> <dt>

*lParam* 
</dt> <dd>

La structure **Rect** pour contenir un rectangle de fenêtre d’info-bulle ou un rectangle d’affichage de texte.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro si le rectangle est correctement ajusté et retourne zéro si une erreur se produit.

## <a name="remarks"></a>Notes

Ce message est particulièrement utile lorsque vous souhaitez utiliser un contrôle ToolTip pour afficher le texte intégral d’une chaîne habituellement tronquée. Elle est couramment utilisée avec les contrôles ListView et TreeView. En général, vous envoyez ce message en réponse à un code de notification [ttn \_ Show](ttn-show.md) afin que vous puissiez positionner le contrôle ToolTip correctement.

Le rectangle de la fenêtre d’info-bulle est un peu plus grand que le rectangle d’affichage de texte qui délimite la chaîne d’info-bulle. L’origine de la fenêtre est également décalée vers le haut et vers la gauche à partir de l’origine du rectangle d’affichage de texte. Pour positionner le rectangle d’affichage du texte, vous devez calculer le rectangle de la fenêtre correspondante et utiliser ce rectangle pour positionner l’info-bulle. **Atténuation \_ ADJUSTRECT** gère ce calcul pour vous.

Si vous affectez à *wParam* la **valeur true**, **atténuation \_ ADJUSTRECT** prend la taille et la position du rectangle d’info-bulle souhaité, et transmet la taille et la position de la fenêtre d’info-bulle nécessaire pour afficher le texte à la position spécifiée. Si vous affectez à *wParam* la **valeur false**, vous pouvez spécifier un rectangle de fenêtre d’info-bulle et **atténuation \_ ADJUSTRECT** retourne la taille et la position de son rectangle de texte.

Le fragment de code suivant illustre l’utilisation du message **atténuation \_ ADJUSTRECT** pour positionner un contrôle ToolTip afin d’afficher le texte complet de la chaîne d’un contrôle à la place d’une chaîne tronquée. La fonction **GetMyItemRect** définie par l’application retourne le rectangle de texte qui sera nécessaire pour afficher le texte info-bulle directement sur la chaîne tronquée. Les détails de l’implémentation de cette fonction dépendent du contrôle particulier. **Atténuation \_ ADJUSTRECT** est utilisé pour envoyer ce rectangle de texte au contrôle ToolTip. Elle retourne un rectangle de fenêtre de taille et de position approprié qui est ensuite utilisé pour positionner la fenêtre d’info-bulle.


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





