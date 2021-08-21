---
title: Message MCM_SETCURRENTVIEW (commctrl. h)
description: Définit la vue actuelle du calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cf7206fb7e778c0ab7d28ee8947b9327e8cc98bd8ae8c9063213814676a77e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019037"
---
# <a name="mcm_setcurrentview-message"></a>\_Message SETCURRENTVIEW MCM

Définit la vue actuelle du calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle vue. Une des constantes suivantes.



| Valeur                                                                                                                                                      | Signification                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**MCMV \_ mois**</dt> </dl>       | Affichage mensuel.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**MCMV \_ année**</dt> </dl>          | Vue annuelle.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**MCMV \_ décennie**</dt> </dl>    | Vue décennie.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**MCMV \_ siècle**</dt> </dl> | Vue Century.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





