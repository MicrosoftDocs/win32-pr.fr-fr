---
title: Message TDM_SET_PROGRESS_BAR_STATE (commctrl. h)
description: Définit l’état de la barre de progression dans une boîte de dialogue de tâche.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2021
ms.locfileid: "104321790"
---
# <a name="tdm_set_progress_bar_state-message"></a>Message d’état de la barre de progression de l' \_ ensemble TDM \_ \_ \_

Définit l’état de la barre de progression dans une boîte de dialogue de tâche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

**Entier** qui spécifie l’état de la barre de progression. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                   | Signification                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ normal**</dt> </dl> | Définit la barre de progression à l’état normal.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ suspendu**</dt> </dl>    | Définit la barre de progression à l’état suspendu.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**\_erreur PBST**</dt> </dl>    | Définissez la barre de progression sur l’état d’erreur.<br/>   |



 

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour recevoir l’appel d’informations d’erreur étendues GetLastError.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





