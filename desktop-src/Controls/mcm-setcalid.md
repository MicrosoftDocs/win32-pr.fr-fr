---
title: Message MCM_SETCALID (commctrl. h)
description: Définit l’ID de calendrier pour le contrôle de calendrier donné. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032493"
---
# <a name="mcm_setcalid-message"></a>\_Message SETCALID MCM

Définit l’ID de calendrier pour le contrôle de calendrier donné. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

ID de calendrier. Une des constantes d' [identificateurs de calendrier](/windows/desktop/Intl/calendar-identifiers) .

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Inutilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

