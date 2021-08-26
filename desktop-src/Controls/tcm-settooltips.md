---
title: Message TCM_SETTOOLTIPS (commctrl. h)
description: Assigne un contrôle ToolTip à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetToolTips.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS les contrôles de Windows de message
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
ms.openlocfilehash: c8bfec3b7272ceae3dcbf1781e3bb17a988f2252b3c0a74822677bff6ea39209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104689"
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

## <a name="remarks"></a>Remarques

Vous pouvez récupérer le contrôle ToolTip associé à un contrôle onglet à l’aide du message [**\_ GETTOOLTIPS TCM**](tcm-gettooltips.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





