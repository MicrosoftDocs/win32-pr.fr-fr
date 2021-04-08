---
title: ACN_START le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle d’animation que le clip AVI associé a démarré. Ce code de notification est envoyé sous la forme d’un \_ message de commande WM.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- Contrôles Windows de code de notification ACN_START
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740517"
---
# <a name="acn_start-notification-code"></a>ACN \_ Démarrer le code de notification

Avertit la fenêtre parente d’un contrôle d’animation que le clip AVI associé a démarré. Ce code de notification est envoyé sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’animation. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWND** qui spécifie le handle du contrôle d’animation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

