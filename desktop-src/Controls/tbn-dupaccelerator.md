---
title: TBN_DUPACCELERATOR le code de notification (commctrl. h)
description: Détermine si une touche d’accès rapide peut être utilisée sur au moins deux barres d’outils actives. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- Contrôles Windows de code de notification TBN_DUPACCELERATOR
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
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033089"
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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





