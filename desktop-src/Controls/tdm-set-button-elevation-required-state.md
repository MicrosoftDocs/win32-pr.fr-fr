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
ms.openlocfilehash: 2c69998da085a74b144179a0a4244c787cd3a871d63eca1e5df9c4e555b1a7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104619"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





