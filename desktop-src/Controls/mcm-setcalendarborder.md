---
title: Message MCM_SETCALENDARBORDER (commctrl. h)
description: Définit la taille de la bordure, en pixels. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER les contrôles de message Windows
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
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465247"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





