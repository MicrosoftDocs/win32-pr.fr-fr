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
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116034"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

L’exemple de la section syntaxe montre le cast en wParam avant l’envoi de la notification. **LParam** n’est pas utilisé et doit être égal à zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





