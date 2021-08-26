---
title: TBN_WRAPACCELERATOR le code de notification (commctrl. h)
description: Demande l’index du bouton dans une ou plusieurs barres d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c5ec222f387108e2cb4d240e6dddf0fcb904d814097a96624a177425eb805ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105029"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>\_Code de notification TBN WRAPACCELERATOR

Demande l’index du bouton dans une ou plusieurs barres d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure qui contient le caractère de touche accélérateur et qui reçoit l’index du bouton correspondant. L’index est-1 si l’accélérateur ne correspond pas à une commande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**True** si un index est retourné ; sinon, **false**.

## <a name="remarks"></a>Remarques

Les applications avec une ou plusieurs barres d’outils peuvent recevoir ce code de notification.

La structure **NMTBWRAPACCELERATOR** doit être définie par l’application comme suit :

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





