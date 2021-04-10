---
title: Message DTM_GETMONTHCAL (commctrl. h)
description: Obtient le handle vers le contrôle de calendrier mensuel de l’enfant du sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetMonthCal.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- DTM_GETMONTHCAL les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942491"
---
# <a name="dtm_getmonthcal-message"></a>\_Message DTM GETMONTHCAL

Obtient le handle vers le contrôle de calendrier mensuel de l’enfant du sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle calendrier mensuel enfant d’un contrôle PAO en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Notes

Les contrôles de PAO créent un contrôle calendrier mensuel enfant lorsque l’utilisateur clique sur la flèche déroulante (notification de[ \_ liste déroulante DTN](dtn-dropdown.md) ). Lorsque le calendrier mensuel n’est plus nécessaire, il est détruit (une notification [DTN \_ gros plan](dtn-closeup.md) est envoyée lors de la destruction). Par conséquent, votre application ne doit pas s’appuyer sur un handle statique du calendrier du mois enfant du contrôle PAO.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[DTN \_ gros plan](dtn-closeup.md)
</dt> <dt>

[\_liste déroulante DTN](dtn-dropdown.md)
</dt> </dl>

 

 





