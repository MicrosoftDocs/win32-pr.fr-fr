---
title: TBN_QUERYDELETE le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être supprimé d’une barre d’outils pendant que l’utilisateur personnalise la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116277"
---
# <a name="tbn_querydelete-notification-code"></a>\_Code de notification TBN QUERYDELETE

Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être supprimé d’une barre d’outils pendant que l’utilisateur personnalise la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Le membre **iItem** contient l’index de base zéro du bouton à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** pour autoriser la suppression du bouton ou **false** pour empêcher la suppression du bouton.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





