---
description: Avertit une application quand un IME sélectionné a besoin d’informations sur la fenêtre de composition. L’application reçoit cette commande via le \_ message de \_ demande de l’IME WM avec les paramètres définis comme indiqué ci-dessous.
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: IMR_COMPOSITIONWINDOW le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533876"
---
# <a name="imr_compositionwindow-notification-code"></a>\_Code de notification IMR COMPOSITIONWINDOW

Avertit une application quand un IME sélectionné a besoin d’informations sur la fenêtre de composition. L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres définis comme indiqué ci-dessous.


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Définissez sur IMR \_ COMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une mémoire tampon contenant une structure [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur différente de zéro si l’application remplit la structure [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) . Dans le cas contraire, la commande retourne 0.

## <a name="remarks"></a>Notes

Cette commande peut être envoyée par l’IME à une fenêtre qui a effacé l' \_ indicateur ISC SHOWUICOMPOSITIONWINDOW dans le gestionnaire de messages [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>IMM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Commandes du gestionnaire de méthode d’entrée](input-method-manager-commands.md)
</dt> <dt>

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**demande de l' \_ IME WM \_**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 




