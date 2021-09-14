---
title: Message TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (commctrl. h)
description: Spécifie si un lien de commande ou un bouton de boîte de dialogue de tâche donné doit avoir une icône de protection de contrôle de compte d’utilisateur (UAC). autrement dit, si l’action appelée par le bouton requiert une élévation.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116085"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>Message d’état d’élévation de bouton de l' \_ ensemble TDM \_ \_ \_ requis \_

Spécifie si un lien de commande ou un bouton de boîte de dialogue de tâche donné doit avoir une icône de protection de contrôle de compte d’utilisateur (UAC). autrement dit, si l’action appelée par le bouton requiert une élévation.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

ID du bouton de commande ou du lien de commande à mettre à jour.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Affectez la valeur 0 pour indiquer que l’action appelée par le bouton ne requiert pas d’élévation. Définissez sur une valeur différente de zéro pour indiquer que l’action requiert une élévation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





