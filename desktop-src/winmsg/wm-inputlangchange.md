---
description: Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée. Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction DefWindowProc, qui le transmet à toutes les fenêtres enfants de premier niveau.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE, message (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f56367045fe72a8288220e1aeef662e648d702c3b48ead23bf179142dff92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436244"
---
# <a name="wm_inputlangchange-message"></a>\_Message WM INPUTLANGCHANGE

Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée. Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , qui le transmet à toutes les fenêtres enfants de premier niveau. Ces fenêtres enfants peuvent transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour qu’il transmette le message à leurs fenêtres enfants, et ainsi de suite.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam*

</dt> <dd>
  
Type : **wParam**

[Page de codes](../Intl/code-pages.md) des nouveaux paramètres régionaux.

</dd> <dt>

*lParam*

</dt> <dd>
 
Type : **lParam**

Identificateur de paramètres régionaux d’entrée **HKL** . Pour plus d’informations, consultez [langues, paramètres régionaux et dispositions de clavier](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner une valeur différente de zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Vous pouvez récupérer le [nom des paramètres régionaux](../Intl/locale-names.md) du clavier via la fonction [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) . Avec le nom des paramètres régionaux, vous pouvez utiliser les [fonctions de paramètres régionaux modernes](/windows/win32/intl/calling-the--locale-name--functions):

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |

## <a name="see-also"></a>Voir aussi

**Référence**

- [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [**\_INPUTLANGCHANGEREQUEST WM**](wm-inputlangchangerequest.md)

**Méthodologique**

- [Windows](windows.md) 
