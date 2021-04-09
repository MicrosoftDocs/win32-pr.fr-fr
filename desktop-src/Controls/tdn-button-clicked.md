---
title: TDN_BUTTON_CLICKED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne un bouton ou un lien de commande dans la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- Contrôles Windows de code de notification TDN_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942842"
---
# <a name="tdn_button_clicked-notification-code"></a>\_Clic sur le bouton TDN du \_ Code de notification

Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne un bouton ou un lien de commande dans la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Entier** qui spécifie l’ID du bouton ou du lien de la connexion qui a été sélectionné.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour empêcher la fermeture de la boîte de dialogue de tâche, l’application doit retourner la **\_ valeur false**, sinon la boîte de dialogue de tâche est fermée et l’ID de bouton est retourné via l’appel d’application d’origine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





