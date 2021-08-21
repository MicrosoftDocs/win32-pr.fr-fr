---
title: TBN_DUPACCELERATOR le code de notification (commctrl. h)
description: Détermine si une touche d’accès rapide peut être utilisée sur au moins deux barres d’outils actives. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ff0059a6071db79cab91fcf903a1e68f3550c766b3d16cd3571c3a785e7368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829326"
---
# <a name="tbn_dupaccelerator-notification-code"></a>\_Code de notification TBN DUPACCELERATOR

Détermine si une touche d’accès rapide peut être utilisée sur au moins deux barres d’outils actives. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure qui fournit un accélérateur et qui reçoit une valeur spécifiant si plusieurs barres d’outils répondent au même caractère.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, sinon **false**.

## <a name="remarks"></a>Remarques

L’application doit déclarer la structure **NMTBDUPACCELERATOR** comme suit :

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





