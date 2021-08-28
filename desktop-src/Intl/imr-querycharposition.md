---
description: Avertit une application lorsque l’IME sélectionné a besoin d’informations sur les coordonnées d’un caractère dans la chaîne de composition. L’application reçoit cette commande via le \_ \_ message de demande de l’IME WM avec les paramètres de paramètre, comme indiqué ci-dessous.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: IMR_QUERYCHARPOSITION le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a37679dce6a17d5687aeed1c8fbd1d5c8bf6651b3cfc597cfdfc2e419ecba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948766"
---
# <a name="imr_querycharposition-notification-code"></a>\_Code de notification IMR QUERYCHARPOSITION

Avertit une application lorsque l’IME sélectionné a besoin d’informations sur les coordonnées d’un caractère dans la chaîne de composition. L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres de paramètre, comme indiqué ci-dessous.


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Définissez sur IMR \_ QUERYCHARPOSITION.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Pointeur vers une structure [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) qui contient la position du caractère dans la fenêtre de composition.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur différente de zéro si l’application remplit la structure [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . Dans le cas contraire, la commande retourne 0.

## <a name="remarks"></a>Remarques

Une application qui dessine la chaîne de composition elle-même, au lieu de s’appuyer sur l’IME, est responsable du remplissage de tous les membres de la structure [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . Dans le cas contraire, l’application doit passer la commande à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) si elle possède sa propre fenêtre d’interface utilisateur IME.

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

[**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[**demande de l' \_ IME WM \_**](wm-ime-request.md)
</dt> </dl>

 

 
