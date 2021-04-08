---
title: Message MCM_GETMAXSELCOUNT (commctrl. h)
description: Récupère la plage de dates maximale pouvant être sélectionnée dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- MCM_GETMAXSELCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033014"
---
# <a name="mcm_getmaxselcount-message"></a>\_Message GETMAXSELCOUNT MCM

Récupère la plage de dates maximale pouvant être sélectionnée dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui représente le nombre total de jours pouvant être sélectionnés pour le contrôle.

## <a name="remarks"></a>Notes

Vous pouvez modifier la plage de dates maximale pouvant être sélectionnée à l’aide du message [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





