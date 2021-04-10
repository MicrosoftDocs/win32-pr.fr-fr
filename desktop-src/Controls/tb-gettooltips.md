---
title: Message TB_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip, le cas échéant, associé à la barre d’outils.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032942"
---
# <a name="tb_gettooltips-message"></a>TO \_ GETTOOLTIPS message

Récupère le handle du contrôle ToolTip, le cas échéant, associé à la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle ToolTip, ou **null** si la barre d’outils n’est associée à aucune info-bulle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





