---
description: Avertit une application lorsque le mode de conversion du contexte d’entrée est mis à jour. L’application reçoit cette commande via le \_ message de \_ notification de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: IMN_SETCONVERSIONMODE le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526236"
---
# <a name="imn_setconversionmode-notification-code"></a>\_Code de notification SETCONVERSIONMODE IMN

Avertit une application lorsque le mode de conversion du contexte d’entrée est mis à jour. L’application reçoit cette commande via le message de [**\_ \_ notification de l’IME WM**](wm-ime-notify.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Défini sur IMN \_ SETCONVERSIONMODE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette commande n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

L’application peut obtenir des informations sur le mode de conversion à l’aide de la fonction [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .

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

[**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**notification de l' \_ IME WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




