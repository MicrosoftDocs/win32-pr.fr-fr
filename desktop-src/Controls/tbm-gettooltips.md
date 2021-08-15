---
title: Message TBM_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip assigné au TrackBar, le cas échéant.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS les contrôles de Windows de message
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
ms.openlocfilehash: 4c97c94ab3a696f5967f724e76d2d8702a01275bedc06ad7c13907d57710a078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078063"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





