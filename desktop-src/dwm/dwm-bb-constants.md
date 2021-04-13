---
title: Brouilleur de DWM derrière les constantes (dwmapi. h)
description: Indicateurs utilisés par la \_ structure DWM BLURBEHIND pour indiquer les membres qui contiennent des informations valides.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508810"
---
# <a name="dwm-blur-behind-constants"></a>Brouilleur de DWM derrière les constantes

Indicateurs utilisés par la structure [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) pour indiquer les membres qui contiennent des informations valides.

<dl> <dt>

<span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ activé**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Une valeur a été spécifiée pour le membre **fEnable** .


</dt> </dl> </dd> <dt>

<span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Une valeur a été spécifiée pour le membre **hRgnBlur** .


</dt> </dl> </dd> <dt>

<span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Une valeur a été spécifiée pour le membre **fTransitionOnMaximized** .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Dwmapi. h</dt> </dl> |



 

 





