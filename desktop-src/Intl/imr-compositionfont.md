---
description: Avertit une application quand un IME sélectionné a besoin d’informations sur la police utilisée par la fenêtre de composition. L’application reçoit cette commande via le \_ message de \_ requête de l’IME WM avec les paramètres, comme indiqué ci-dessous.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: IMR_COMPOSITIONFONT le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527877"
---
# <a name="imr_compositionfont-notification-code"></a>\_Code de notification IMR COMPOSITIONFONT

Avertit une application quand un IME sélectionné a besoin d’informations sur la police utilisée par la fenêtre de composition. L’application reçoit cette commande via le message de [**\_ \_ requête de l’IME WM**](wm-ime-request.md) avec les paramètres, comme indiqué ci-dessous.


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Définissez sur IMR \_ COMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une mémoire tampon contenant une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . L’application remplit les valeurs de la fenêtre de composition actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur différente de zéro si l’application remplit la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Dans le cas contraire, la commande retourne 0.

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

[**demande de l' \_ IME WM \_**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 
