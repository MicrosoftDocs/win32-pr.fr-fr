---
title: TDN_HYPERLINK_CLICKED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche quand l’utilisateur clique sur un lien hypertexte dans le contenu de la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- Contrôles Windows de code de notification TDN_HYPERLINK_CLICKED
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106234"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a>\_Code de \_ notification de clic sur le lien hypertexte TDN

Envoyé par une boîte de dialogue de tâche quand l’utilisateur clique sur un lien hypertexte dans le contenu de la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne de caractères larges contenant l’URL du lien hypertexte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





