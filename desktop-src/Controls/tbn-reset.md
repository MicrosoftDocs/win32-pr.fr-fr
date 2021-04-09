---
title: TBN_RESET le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils que l’utilisateur a réinitialisé le contenu de la boîte de dialogue Personnaliser la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- Contrôles Windows de code de notification TBN_RESET
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033201"
---
# <a name="tbn_reset-notification-code"></a>\_Code de notification de réinitialisation TBN

Avertit la fenêtre parente de la barre d’outils que l’utilisateur a réinitialisé le contenu de la boîte de dialogue Personnaliser la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Return TBNRF \_ ENDCUSTOMIZE pour fermer la boîte de dialogue Personnaliser la barre d’outils. Toutes les autres valeurs de retour sont ignorées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





