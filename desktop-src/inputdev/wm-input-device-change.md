---
title: Message WM_INPUT_DEVICE_CHANGE (winuser. h)
description: Envoyé à la fenêtre qui s’est inscrite pour recevoir une entrée brute. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823aeaf5655703802f07fb238d5c6c5dc479defa12ae4a416423b4519fd2b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247885"
---
# <a name="wm_input_device_change-message"></a>Message WM_INPUT_DEVICE_CHANGE

## <a name="description"></a>Description

Envoyé à la fenêtre qui s’est inscrite pour recevoir une entrée brute. 

Les notifications d’entrée brutes ne sont disponibles qu’une fois que l’application a appelé [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) avec [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) indicateur.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam*

</dt> <dd>

Type : **wParam**

Ce paramètre peut prendre les valeurs suivantes.

| Valeur                    | Signification                                    |
|--------------------------|--------------------------------------------|
| **\_arrivée GIDC** </br>1 | Un nouvel appareil a été ajouté au système. </br> Vous pouvez appeler [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) pour obtenir plus d’informations sur l’appareil. |
| **suppression de GIDC \_** </br>2 | Un appareil a été supprimé du système. |

</dd> <dt>

*lParam* 

</dt> <dd>

Type : **lParam**

**Handle** de l’appareil d’entrée brut.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="see-also"></a>Voir aussi

**Méthodologique**

[Entrée brute](/windows/desktop/inputdev/raw-input)

**Référence**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[RAWINPUTDEVICE, structure](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

