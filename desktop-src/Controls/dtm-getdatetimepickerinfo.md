---
title: Message DTM_GETDATETIMEPICKERINFO (commctrl. h)
description: Obtient des informations sur un contrôle de sélecteur de dates et d’heures (PAO).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- DTM_GETDATETIMEPICKERINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48dc639a48455564b9f925f7d6eea9634c01e597323f81d951cfde372a34ea37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878219"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>\_Message DTM GETDATETIMEPICKERINFO

Obtient des informations sur un contrôle de sélecteur de dates et d’heures (PAO).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd> Pointeur vers <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> pour recevoir les informations. L’appelant est chargé d’allouer la mémoire pour cette structure. Définissez le membre **cbSize** de la structure sur sizeof (DATETIMEPICKERINFO) avant d’envoyer ce message.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





