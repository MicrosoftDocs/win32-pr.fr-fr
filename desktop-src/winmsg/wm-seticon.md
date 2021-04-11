---
description: Associe une nouvelle grande ou petite icône à une fenêtre. Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Message WM_SETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202878"
---
# <a name="wm_seticon-message"></a>\_Message WM SETICON

Associe une nouvelle grande ou petite icône à une fenêtre. Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type d’icône à définir. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                       | Signification                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Icône \_ BIG**</dt> <dt>1</dt> </dl>       | Définissez la grande icône pour la fenêtre.<br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Icône \_ PETIT**</dt> <dt>0</dt> </dl> | Définissez la petite icône pour la fenêtre.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la nouvelle icône de grande taille ou petite. Si ce paramètre a la **valeur null**, l’icône indiquée par *wParam* est supprimée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

La valeur de retour est un handle vers la grande icône précédente ou petite, en fonction de la valeur de *wParam*. La **valeur est null** si la fenêtre n’avait pas précédemment d’icône de type indiquée par *wParam*.

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne un descripteur à la grande ou petite icône précédente associée à la fenêtre, en fonction de la valeur de *wParam*.

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

[**\_GETICON WM**](wm-geticon.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
