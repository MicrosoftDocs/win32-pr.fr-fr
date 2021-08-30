---
title: TDN_EXPANDO_BUTTON_CLICKED le code de notification (commctrl. h)
description: Envoyé par la boîte de dialogue de tâche lorsque l’utilisateur clique sur le bouton développé de la boîte de dialogue. Cette notification est reçue uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- TDN_EXPANDO_BUTTON_CLICKED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac901777ab7599592e5646946f19d9e2456b6afbe911645259adbf7459e3995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875779"
---
# <a name="tdn_expando_button_clicked-notification-code"></a>\_Bouton TDN expando- \_ \_ clic sur le code de notification

Envoyé par la boîte de dialogue de tâche lorsque l’utilisateur clique sur le bouton développé de la boîte de dialogue. Cette notification est reçue uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **booléenne** qui est **true** si la boîte de dialogue est développée, ou **false** dans le cas contraire.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

L’exemple de la section syntaxe montre le cast en wParam avant l’envoi de la notification. **LParam** n’est pas utilisé et doit être égal à zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





