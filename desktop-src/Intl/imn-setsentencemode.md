---
description: Avertit une application lorsque le mode de phrase du contexte d’entrée est mis à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 72455193-cd17-45f8-b19c-a1f735ff81bf
title: IMN_SETSENTENCEMODE le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a5fa976bbd28e86d5b46eec074e5ed802cc0a32e1c7c1c86b0e01a4629fe13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145945"
---
# <a name="imn_setsentencemode-notification-code"></a>\_Code de notification SETSENTENCEMODE IMN

Avertit une application lorsque le mode de phrase du contexte d’entrée est mis à jour. L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
IMN_SETSENTENCEMODE
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMN \_ SETSENTENCEMODE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette commande n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

L’application peut obtenir des informations sur le mode phrase à l’aide de la fonction [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .

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

[**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**notification de l' \_ IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




