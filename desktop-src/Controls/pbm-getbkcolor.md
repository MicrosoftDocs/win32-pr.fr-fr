---
title: Message PBM_GETBKCOLOR (commctrl. h)
description: Obtient la couleur d’arrière-plan de la barre de progression.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117730"
---
# <a name="pbm_getbkcolor-message"></a>\_Message PBM GETBKCOLOR

Obtient la couleur d’arrière-plan de la barre de progression.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la couleur d’arrière-plan de la barre de progression.

## <a name="remarks"></a>Notes

Il s’agit de la couleur définie par le message [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md) . La valeur par défaut est CLR \_ par défaut, qui est définie dans commctrl. h.

Cette fonction affecte uniquement le mode classique, et non aucun style visuel.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





