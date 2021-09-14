---
description: Le \_ message WM PALETTECHANGED est envoyé à toutes les fenêtres de niveau supérieur et Overlapped une fois que la fenêtre avec le focus clavier a réalisé sa palette logique, ce qui modifie la palette du système.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Message WM_PALETTECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414310"
---
# <a name="wm_palettechanged-message"></a>\_Message WM PALETTECHANGED

Le message **WM \_ PALETTECHANGED** est envoyé à toutes les fenêtres de niveau supérieur et Overlapped une fois que la fenêtre avec le focus clavier a réalisé sa palette logique, ce qui modifie la palette du système. Ce message active une fenêtre qui utilise une palette de couleurs, mais n’a pas le focus clavier pour réaliser sa palette logique et mettre à jour sa zone cliente.

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

Handle de la fenêtre qui a provoqué la modification de la palette système.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Ce message doit être envoyé à toutes les fenêtres de niveau supérieur et avec chevauchement, y compris celui qui a modifié la palette du système. Si des fenêtres enfants utilisent une palette de couleurs, ce message doit également leur être transmis.

Pour éviter de créer une boucle infinie, une fenêtre qui reçoit ce message ne doit pas réaliser sa palette, sauf si elle détermine que *wParam* ne contient pas son propre handle de fenêtre.

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

[**\_PALETTEISCHANGING WM**](wm-paletteischanging.md)
</dt> <dt>

[**\_QUERYNEWPALETTE WM**](wm-querynewpalette.md)
</dt> </dl>

 

 
