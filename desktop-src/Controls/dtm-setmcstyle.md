---
title: Message DTM_SETMCSTYLE (commctrl. h)
description: Définit le style d’un contrôle de sélecteur de dates et d’heures (PAO). Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104839"
---
# <a name="dtm_setmcstyle-message"></a>\_Message DTM SETMCSTYLE

Définit le style d’un contrôle de sélecteur de dates et d’heures (PAO). Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>Valeur de style. Pour plus d’informations, consultez <a href="month-calendar-control-styles.md">styles du contrôle Month Calendar</a>.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur du style précédent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





