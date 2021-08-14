---
title: Message MCM_SETCALENDARBORDER (commctrl. h)
description: Définit la taille de la bordure, en pixels. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e020ad282ce21555e6c3a74198a0034013ac1d7cfac8f4eb68e52137e5f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697199"
---
# <a name="mcm_setcalendarborder-message"></a>\_Message SETCALENDARBORDER MCM

Définit la taille de la bordure, en pixels. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Si la **valeur est true**, la taille de la bordure est définie sur le nombre de pixels que le *lParam* spécifie. Si la valeur est **false**, la taille de la bordure est réinitialisée à la valeur par défaut spécifiée par le thème, ou zéro si les thèmes ne sont pas utilisés.

</dd> <dt>

*lParam* 
</dt> <dd>

Nombre de pixels de la taille de la bordure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Non utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





