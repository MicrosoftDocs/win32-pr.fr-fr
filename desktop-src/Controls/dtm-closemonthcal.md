---
title: Message DTM_CLOSEMONTHCAL (commctrl. h)
description: Ferme un contrôle de sélecteur de dates et d’heures (PAO). Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124077"
---
# <a name="dtm_closemonthcal-message"></a>\_Message DTM CLOSEMONTHCAL

Ferme un contrôle de sélecteur de dates et d’heures (PAO). Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne zéro.

## <a name="remarks"></a>Notes

Détruit le contrôle et envoie une notification [DTN \_ gros plan](dtn-closeup.md) que le contrôle se ferme, par opposition au fait que le contrôle est en cours d’ouverture (en le déplaçant dans la notification de [ \_ liste déroulante DTN](dtn-dropdown.md) ) vers le parent du contrôle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[\_liste déroulante DTN](dtn-dropdown.md)
</dt> <dt>

[DTN \_ gros plan](dtn-closeup.md)
</dt> </dl>

 

 





