---
title: Message DTM_GETMCSTYLE (commctrl. h)
description: Obtient le style d’un contrôle de sélecteur de date et d’heure (PAO). Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime GetMonthCalStyle.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- DTM_GETMCSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639c573f8a49b0ea2dd4b313b11620fa7fa4bed6c158b85fef3afffcee03bf3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878089"
---
# <a name="dtm_getmcstyle-message"></a>\_Message DTM GETMCSTYLE

Obtient le style d’un contrôle de sélecteur de date et d’heure (PAO). Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de style du contrôle. Pour plus d’informations, consultez [styles du contrôle Month Calendar](month-calendar-control-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





