---
title: TDN_TIMER le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche environ toutes les 200 millisecondes.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116010"
---
# <a name="tdn_timer-notification-code"></a>\_Code de notification du minuteur TDN

Envoyé par une boîte de dialogue de tâche environ toutes les 200 millisecondes. Ce code de notification est envoyé lorsque l' \_ indicateur de minuterie de rappel TDF \_ a été défini dans le membre **dwFlags** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) qui a été passée à la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode **TaskDialogIndirect** .


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Valeur DWORD** qui spécifie le nombre de millisecondes écoulées depuis la création de la boîte de dialogue ou si le code de notification a retourné la **\_ valeur false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour réinitialiser le TickCount, l’application doit retourner **la \_ valeur false**, sinon le TickCount continue à s’incrémenter.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





