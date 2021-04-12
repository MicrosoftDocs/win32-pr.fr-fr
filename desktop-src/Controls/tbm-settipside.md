---
title: Message TBM_SETTIPSIDE (commctrl. h)
description: Positionne un contrôle ToolTip utilisé par un contrôle TrackBar. Les contrôles TrackBar qui utilisent le \_ style des info-bulles tbs affichent des info-bulles.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- TBM_SETTIPSIDE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384263"
---
# <a name="tbm_settipside-message"></a>\_Message TBM SETTIPSIDE

Positionne un contrôle ToolTip utilisé par un contrôle TrackBar. Les contrôles TrackBar qui utilisent le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) affichent des info-bulles.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur représentant l’emplacement d’affichage du contrôle ToolTip. Cette valeur peut être l'une des suivantes :



| Valeur                                                                                                                                                   | Signification                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <dt>**TBTS \_ Top**</dt> </dl>          | Le contrôle ToolTip est positionné au-dessus du TrackBar. Cet indicateur est destiné à être utilisé avec le trackbars horizontal.<br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <dt>**TBTS \_ gauche**</dt> </dl>       | Le contrôle ToolTip sera positionné à gauche du TrackBar. Cet indicateur est destiné à être utilisé avec le trackbars vertical.<br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <dt>**TBTS \_ bas**</dt> </dl> | Le contrôle ToolTip sera positionné sous le TrackBar. Cet indicateur est destiné à être utilisé avec le trackbars horizontal.<br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <dt>**TBTS \_ droit**</dt> </dl>    | Le contrôle ToolTip est positionné à droite du TrackBar. Cet indicateur est destiné à être utilisé avec le trackbars vertical.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur qui représente l’emplacement précédent du contrôle ToolTip. La valeur de retour est égale à l’une des valeurs possibles pour *wParam*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





