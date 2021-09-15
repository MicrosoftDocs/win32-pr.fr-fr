---
description: Envoyé lorsque la taille et la position de la zone cliente d’une fenêtre doivent être calculées. En traitant ce message, une application peut contrôler le contenu de la zone cliente de la fenêtre lorsque la taille ou la position de la fenêtre change.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: Message WM_NCCALCSIZE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7d63fea3ad0a80bba686d8d86aa5354f0bb45b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525185"
---
# <a name="wm_nccalcsize-message"></a>\_Message WM NCCALCSIZE

Envoyé lorsque la taille et la position de la zone cliente d’une fenêtre doivent être calculées. En traitant ce message, une application peut contrôler le contenu de la zone cliente de la fenêtre lorsque la taille ou la position de la fenêtre change.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Si *wParam* a la **valeur true**, il spécifie que l’application doit indiquer la partie de la zone cliente qui contient des informations valides. Le système copie les informations valides dans la zone spécifiée au sein de la nouvelle zone cliente.

Si *wParam* a la **valeur false**, l’application n’a pas besoin d’indiquer la partie valide de la zone cliente.

</dd> <dt>

*lParam* 
</dt> <dd>

Si *wParam* a la **valeur true**, *lParam* pointe vers une structure [**NCCALCSIZE \_ params**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) qui contient des informations qu’une application peut utiliser pour calculer la nouvelle taille et la position du rectangle client.

Si *wParam* a la **valeur false**, *lParam* pointe vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) . À l’entrée, la structure contient le rectangle de fenêtre proposé pour la fenêtre. À la sortie, la structure doit contenir les coordonnées d’écran de la zone cliente de fenêtre correspondante.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **LRESULT**

Si le paramètre *wParam* a la **valeur false**, l’application doit retourner la valeur zéro.

Si *wParam* a la **valeur true**, l’application doit retourner zéro ou une combinaison des valeurs suivantes.

Si *wParam* a la **valeur true** et qu’une application retourne zéro, l’ancienne zone client est conservée et est alignée avec l’angle supérieur gauche de la nouvelle zone cliente.



| Code/valeur de retour                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ ALIGNTOP**</dt> <dt>0x0010</dt> </dl>    | Spécifie que la zone cliente de la fenêtre doit être conservée et alignée avec le haut de la nouvelle position de la fenêtre. Par exemple, pour aligner la zone client dans le coin supérieur gauche, renvoyez les \_ valeurs WVR ALIGNTOP et **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ ALIGNRIGHT**</dt> <dt>0x0080</dt> </dl>  | Spécifie que la zone cliente de la fenêtre doit être conservée et alignée sur le côté droit de la nouvelle position de la fenêtre. Par exemple, pour aligner la zone client dans le coin inférieur droit, retournez les valeurs de **WVR \_ ALIGNRIGHT** et WVR \_ ALIGNBOTTOM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_**</dt> <dt>0x0020</dt> ALIGNLEFT </dl>   | Spécifie que la zone cliente de la fenêtre doit être conservée et alignée sur le côté gauche de la nouvelle position de la fenêtre. Par exemple, pour aligner la zone client dans le coin inférieur gauche, retournez les valeurs de **WVR \_ ALIGNLEFT** et **WVR \_ ALIGNBOTTOM** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_**</dt> <dt>0x0040</dt> ALIGNBOTTOM </dl> | Spécifie que la zone cliente de la fenêtre doit être conservée et alignée en bas de la nouvelle position de la fenêtre. Par exemple, pour aligner la zone client sur l’angle supérieur gauche, renvoyez les \_ valeurs WVR ALIGNTOP et **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_ HREDRAW**</dt> <dt>0x0100</dt> </dl>     | Utilisé en combinaison avec d’autres valeurs, à l’exception de **WVR \_ VALIDRECTS**, provoque le redessin complet de la fenêtre si le rectangle client change de taille horizontalement. Cette valeur est similaire au style de classe [cs \_ HREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_ VREDRAW**</dt> <dt>0x0200</dt> </dl>     | Utilisé en combinaison avec d’autres valeurs, à l’exception de **WVR \_ VALIDRECTS**, provoque le redessin complet de la fenêtre si le rectangle client change de taille verticalement. Cette valeur est similaire au style de classe [cs \_ VREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_ Redessiner**</dt> <dt>0x0300</dt> </dl>      | Cette valeur entraîne le redessin de la fenêtre entière. Il s’agit d’une combinaison de valeurs **WVR \_ HREDRAW** et **WVR \_ VREDRAW** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_ VALIDRECTS**</dt> <dt>0x0400</dt> </dl>  | Cette valeur indique que, lors du retour de [**WM \_ NCCALCSIZE**](wm-nccalcsize.md), les rectangles spécifiés par les membres **rgrc** \[ 1 \] et **rgrc** \[ 2 \] de la structure [**NCCALCSIZE \_ params**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) contiennent respectivement des rectangles de destination et de zone source valides. Le système combine ces rectangles pour calculer la zone de la fenêtre à conserver. Le système copie toute partie de l’image de fenêtre qui se trouve dans le rectangle source et découpe l’image vers le rectangle de destination. Les deux rectangles sont en coordonnées relatives au parent ou à l’écran. Cet indicateur ne peut pas être combiné avec d’autres indicateurs. <br/> Cette valeur de retour permet à une application d’implémenter des stratégies de conservation de la zone client plus élaborées, telles que le centrage ou la conservation d’un sous-ensemble de la zone cliente.<br/> |



 

## <a name="remarks"></a>Notes

La fenêtre peut être redessinée, selon que le style de classe [cs \_ HREDRAW](about-window-classes.md) ou cs \_ VREDRAW est spécifié. Il s’agit du traitement par défaut à compatibilité descendante de ce message par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) (en plus du calcul de rectangle client habituel décrit dans le tableau précédent).

Lorsque *wParam* a la **valeur true**, le retour de 0 sans traitement des rectangles des [**\_ paramètres NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) entraîne le redimensionnement de la zone cliente jusqu’à la taille de la fenêtre, y compris le cadre de la fenêtre. Cela supprime les éléments de la fenêtre et du frame de fenêtre de votre fenêtre, ce qui laisse uniquement la zone cliente affichée.

à compter de Windows Vista, la suppression du frame standard en retournant simplement 0 lorsque *wParam* a la **valeur TRUE** n’affecte pas les frames qui sont étendus dans la zone cliente à l’aide de la fonction [**DwmExtendFrameIntoClientArea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Seul le frame standard sera supprimé.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**\_paramètres NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
