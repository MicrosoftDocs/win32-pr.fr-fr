---
title: TBN_WRAPHOTITEM le code de notification (commctrl. h)
description: Avertit une application avec au moins deux barres d’outils que l’élément réactif est sur le point de changer. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116246"
---
# <a name="tbn_wraphotitem-notification-code"></a>\_Code de notification TBN WRAPHOTITEM

Avertit une application avec au moins deux barres d’outils que l’élément réactif est sur le point de changer. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure qui contient l’ancien élément réactif (**iStart**) et si le nouvel élément réactif est avant (**iDir** =-1) ou après (**iDir** = 1), ainsi que la raison pour laquelle l’élément réactif change.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**True** si l’application gère la modification de l’élément réactif lui-même ; Sinon, **false**.

## <a name="remarks"></a>Notes

La structure **NMTBWRAPHOTITEM** doit être définie par l’application comme suit :

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





