---
title: Message TTM_TRACKACTIVATE (commctrl. h)
description: Active ou désactive une info-bulle de suivi.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- TTM_TRACKACTIVATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942374"
---
# <a name="ttm_trackactivate-message"></a>\_Message atténuation TRACKACTIVATE

Active ou désactive une info-bulle de suivi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur spécifiant si le suivi est activé ou désactivé. Cette valeur peut être l'une des suivantes :



| Valeur                                                                                                                                | Signification                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**:**</dt> </dl>    | Active le suivi.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FAUSSES**</dt> </dl> | Désactiver le suivi.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui identifie l’outil auquel ce message s’applique. Les membres **HWND** et **UID** identifient l’outil, tandis que le membre **cbSize** spécifie la taille de la structure. Tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**ATTÉNUATION \_ TRACKPOSITION**](ttm-trackposition.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 





