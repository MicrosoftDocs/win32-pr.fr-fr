---
title: Message MCM_GETCALENDARCOUNT (commctrl. h)
description: Obtient le nombre de calendriers actuellement affichés dans le contrôle calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104806"
---
# <a name="mcm_getcalendarcount-message"></a>\_Message GETCALENDARCOUNT MCM

Obtient le nombre de calendriers actuellement affichés dans le contrôle calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .

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

Nombre de calendriers actuellement affichés dans le contrôle calendrier. Le nombre maximal de calendriers autorisés est 12.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





