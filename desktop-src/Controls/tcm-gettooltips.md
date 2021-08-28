---
title: Message TCM_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip associé à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetToolTips.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- TCM_GETTOOLTIPS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb68710c13c8b6b236782b133caa5b6f3609fef931e3b1e395b9944e9ab9a651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166932"
---
# <a name="tcm_gettooltips-message"></a>\_Message GETTOOLTIPS TCM

Récupère le handle du contrôle ToolTip associé à un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle ToolTip en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Remarques

Un contrôle onglet crée un contrôle ToolTip s’il a le [**style \_ info-bulles TCS**](tab-control-styles.md) . Vous pouvez également assigner un contrôle ToolTip à un contrôle onglet à l’aide du message [**\_ SETTOOLTIPS TCM**](tcm-settooltips.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





