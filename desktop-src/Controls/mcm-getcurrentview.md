---
title: Message MCM_GETCURRENTVIEW (commctrl. h)
description: Obtient la vue actuelle du calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW les contrôles de Windows de message
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
ms.openlocfilehash: 50f7fce3c1a22ec14ec34e849bd2e3fc4634118b11613913da4e6fae0b9b7b51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319679"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





