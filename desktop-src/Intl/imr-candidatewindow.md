---
description: Notfies une application quand un IME sélectionné a besoin d’informations sur la fenêtre candidate. L’application reçoit cette commande via le \_ \_ message de demande de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9376ff08e0406ff5505107ea1a04cf4e62898660065a8c7fdd54a1b8606850c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810113"
---
# <a name="imr_candidatewindow-notification-code"></a>\_Code de notification IMR CANDIDATEWINDOW

Notfies une application quand un IME sélectionné a besoin d’informations sur la fenêtre candidate. L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Définissez sur IMR \_ CANDIDATEWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une mémoire tampon contenant une structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . Son membre **dwIndex** contient l’index de la fenêtre candidate référencée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur différente de zéro si l’application remplit la structure [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . Dans le cas contraire, la commande retourne 0.

## <a name="remarks"></a>Remarques

Cette commande peut être envoyée par l’IME à une fenêtre qui a effacé l' \_ indicateur ISC SHOWUICANDIDATEWINDOW dans le gestionnaire de messages [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Imm. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Commandes du gestionnaire de méthode d’entrée](input-method-manager-commands.md)
</dt> <dt>

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**demande de l' \_ IME WM \_**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 




