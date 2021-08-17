---
description: Avertit une application lorsque l’IME doit modifier la structure RECONVERTSTRING. L’application reçoit cette commande via le \_ \_ message de demande de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a0fd1c38c7552d09489c51b9acc897f679aa3a218e86bbba222225fcff57e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948796"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>\_Code de notification IMR CONFIRMRECONVERTSTRING

Avertit une application lorsque l’IME doit modifier la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) . L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Définissez sur IMR \_ CONFIRMRECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) à partir de l’IME. Pour plus d'informations, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur différente de zéro si l’application accepte la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modifiée. Dans le cas contraire, la commande retourne 0 et l’IME utilise la structure **RECONVERTSTRING** d’origine.

## <a name="remarks"></a>Remarques

L’application remplit la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) lors de la réception de la commande [IMR \_ RECONVERTSTRING](imr-reconvertstring.md) .

Une fois que l’application a géré [IMR \_ RECONVERTSTRING](imr-reconvertstring.md), l’IME peut ou non ajuster la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) . L’IME envoie une \_ demande de l’IME WM \_ avec **IMR \_ CONFIRMRECONVERTSTRING** pour confirmer les modifications apportées à la structure **RECONVERTSTRING** . Si l’application retourne la **valeur true** pour **IMR \_ CONFIRMRECONVERTSTRING**, l’IME génère une nouvelle chaîne de composition basée sur la structure **RECONVERTSTRING** pour la commande **IMR \_ CONFIRMRECONVERTSTRING** . Si l’application retourne **false** pour **IMR \_ CONFIRMRECONVERTSTRING**, l’IME génère une nouvelle chaîne de composition basée sur la structure **RECONVERTSTRING** d’origine spécifiée par l’application dans la \_ commande IMR RECONVERTSTRING.

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

[IMR \_ RECONVERTSTRING](imr-reconvertstring.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**demande de l' \_ IME WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




