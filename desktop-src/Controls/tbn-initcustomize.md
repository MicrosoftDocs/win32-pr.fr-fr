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
ms.openlocfilehash: b9bbf66e9974e444fd8544e20cb4878e662bb94b4b1f958404794783e52664c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876609"
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

## <a name="return-value"></a>Valeur retournée

Retourne TBNRF \_ HIDEHELP pour supprimer le bouton aide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





