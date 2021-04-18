---
title: TBN_QUERYDELETE le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils qu’un bouton peut être supprimé d’une barre d’outils pendant que l’utilisateur personnalise la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- Contrôles Windows de code de notification TBN_QUERYDELETE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508297"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour autoriser la suppression du bouton ou **false** pour empêcher la suppression du bouton.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





