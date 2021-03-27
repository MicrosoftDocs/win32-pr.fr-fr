---
description: Le \_ message WM PALETTEISCHANGING informe les applications qu’une application va réaliser sa palette logique.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Message WM_PALETTEISCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757876"
---
# <a name="wm_paletteischanging-message"></a>\_Message WM PALETTEISCHANGING

Le message **WM \_ PALETTEISCHANGING** informe les applications qu’une application va réaliser sa palette logique.

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

Handle de la fenêtre qui va réaliser sa palette logique.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

L’application qui modifie sa palette n’attend pas d’accusé de réception de ce message avant de modifier la palette et d’envoyer le message [**WM \_ PALETTECHANGED**](wm-palettechanged.md) . Par conséquent, la palette peut déjà être modifiée quand une application reçoit ce message.

Si l’application ignore ou ne parvient pas à traiter ce message et qu’une deuxième application réalise sa palette alors que le premier utilise des index de palette, il est fort probable que l’utilisateur verra des couleurs inattendues pendant les opérations de dessin suivantes.

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

[**\_QUERYNEWPALETTE WM**](wm-querynewpalette.md)
</dt> </dl>

 

 
