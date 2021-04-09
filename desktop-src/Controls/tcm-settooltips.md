---
title: Message TCM_SETTOOLTIPS (commctrl. h)
description: Assigne un contrôle ToolTip à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetToolTips.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739869"
---
# <a name="tcm_settooltips-message"></a>\_Message SETTOOLTIPS TCM

Assigne un contrôle ToolTip à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du contrôle ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Vous pouvez récupérer le contrôle ToolTip associé à un contrôle onglet à l’aide du message [**\_ GETTOOLTIPS TCM**](tcm-gettooltips.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





