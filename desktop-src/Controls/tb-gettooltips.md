---
title: Message TB_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip, le cas échéant, associé à la barre d’outils.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116693"
---
# <a name="tb_gettooltips-message"></a>TO \_ GETTOOLTIPS message

Récupère le handle du contrôle ToolTip, le cas échéant, associé à la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle du contrôle ToolTip, ou **null** si la barre d’outils n’est associée à aucune info-bulle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





