---
title: Message MCM_GETCURRENTVIEW (commctrl. h)
description: Obtient la vue actuelle du calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466491"
---
# <a name="mcm_getcurrentview-message"></a>\_Message GETCURRENTVIEW MCM

Obtient la vue actuelle du calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Affichage actuel. Une des valeurs suivantes.



| Code de retour                                                                                  | Description              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**MCMV \_ mois**</dt> </dl>   | Affichage mensuel.<br/> |
| <dl> <dt>**MCMV \_ année**</dt> </dl>    | Vue annuelle.<br/>  |
| <dl> <dt>**MCMV \_ décennie**</dt> </dl>  | Vue décennie.<br/>  |
| <dl> <dt>**MCMV \_ siècle**</dt> </dl> | Vue Century.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





