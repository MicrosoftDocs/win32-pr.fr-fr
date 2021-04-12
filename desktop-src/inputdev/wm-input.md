---
title: Message WM_INPUT (winuser. h)
description: Envoyé à la fenêtre qui obtient l’entrée brute. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384420"
---
# <a name="wm_input-message"></a>\_Message d’entrée WM

Envoyé à la fenêtre qui obtient l’entrée brute.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam*

</dt> <dd>

Code d’entrée. Utilisez la macro [**\_ RAWINPUT \_ code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) pour récupérer la valeur.

Peut avoir l’une des valeurs suivantes :

| Valeur | Signification |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**Bord \_ ENTRÉE**</dt> <dt>0</dt> </dl> | Une entrée s’est produite pendant que l’application était au premier plan. </br> L’application doit appeler [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour que le système puisse effectuer un nettoyage. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**Bord \_ INPUTSINK**</dt> <dt>1</dt> </dl> | Une entrée s’est produite alors que l’application ne se trouvait pas au premier plan. |

</dd> <dt>

*lParam* 

</dt> <dd>

Handle **HRAWINPUT** vers la structure [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) qui contient l’entrée brute de l’appareil. Pour récupérer les données brutes, utilisez ce handle dans l’appel à [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Les entrées brutes sont disponibles uniquement quand l’application appelle [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) avec des spécifications de périphérique valides.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|-------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows XP uniquement\] |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2003 \[ uniquement\] |
| En-tête | <dl> <dt>**Winuser. h (inclure Windows. h)**</dt> </dl> |

## <a name="see-also"></a>Voir aussi

**Référence**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**Obtient \_ le \_ wParam de code RAWINPUT \_**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Méthodologique**

[Entrée brute](raw-input.md)
