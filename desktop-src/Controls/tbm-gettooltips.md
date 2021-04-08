---
title: Message TBM_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip assigné au TrackBar, le cas échéant.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843601"
---
# <a name="tbm_gettooltips-message"></a>\_Message TBM GETTOOLTIPS

Récupère le handle du contrôle ToolTip assigné au TrackBar, le cas échéant.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle ToolTip assigné au TrackBar, ou **null** si les info-bulles ne sont pas utilisées. Si le contrôle TrackBar n’utilise pas le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) , la valeur de retour est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





