---
description: Le \_ message WM QUERYNEWPALETTE informe une fenêtre qu’il est sur le point de recevoir le focus clavier, ce qui donne à la fenêtre la possibilité de réaliser sa palette logique lorsqu’il reçoit le focus.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Message WM_QUERYNEWPALETTE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236466"
---
# <a name="wm_querynewpalette-message"></a>\_Message WM QUERYNEWPALETTE

Le message **WM \_ QUERYNEWPALETTE** informe une fenêtre qu’il est sur le point de recevoir le focus clavier, ce qui donne à la fenêtre la possibilité de réaliser sa palette logique lorsqu’il reçoit le focus.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
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

## <a name="return-value"></a>Valeur de retour

Si la fenêtre réalise sa palette logique, elle doit retourner la **valeur true**; Sinon, elle doit retourner **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des couleurs](colors.md)
</dt> <dt>

[Messages de couleur](color-messages.md)
</dt> <dt>

[**\_PALETTECHANGED WM**](wm-palettechanged.md)
</dt> <dt>

[**\_PALETTEISCHANGING WM**](wm-paletteischanging.md)
</dt> </dl>

 

 
