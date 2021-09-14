---
title: TBN_INITCUSTOMIZE le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que la personnalisation a commencé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116282"
---
# <a name="tbn_initcustomize-notification-code"></a>\_Code de notification TBN INITCUSTOMIZE

Avertit la fenêtre parente d’une barre d’outils que la personnalisation a commencé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) de la barre d’outils.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne TBNRF \_ HIDEHELP pour supprimer le bouton aide.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





